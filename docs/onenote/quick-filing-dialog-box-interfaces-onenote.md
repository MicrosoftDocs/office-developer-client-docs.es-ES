---
title: Interfaces de cuadro de diálogo de archivado rápidas (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: En este tema se describe las interfaces que puede usar para personalizar mediante programación el cuadro de diálogo fiscal rápido en OneNote 2013.
ms.openlocfilehash: d2647ed4d7b9f4487c033260eba8df1e4281c6ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816046"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a><span data-ttu-id="77f3d-103">Interfaces de cuadro de diálogo de archivado rápidas (OneNote)</span><span class="sxs-lookup"><span data-stu-id="77f3d-103">Quick Filing dialog box interfaces (OneNote)</span></span>

<span data-ttu-id="77f3d-104">En este tema se describe las interfaces que puede usar para personalizar mediante programación el cuadro de diálogo fiscal rápido en OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="77f3d-104">This topic describes the interfaces that you can use to programmatically customize the Quick Filing dialog box in OneNote 2013.</span></span>
  
## <a name="quick-filing-dialog-box"></a><span data-ttu-id="77f3d-105">Cuadro de diálogo de archivado rápido</span><span class="sxs-lookup"><span data-stu-id="77f3d-105">Quick Filing dialog box</span></span>

<span data-ttu-id="77f3d-106">El cuadro de diálogo fiscal rápido en OneNote 2013 es un cuadro de diálogo personalizable que permite a los usuarios seleccionar una ubicación dentro de la estructura de la jerarquía de OneNote.</span><span class="sxs-lookup"><span data-stu-id="77f3d-106">The Quick Filing dialog box in OneNote 2013 is a customizable dialog box that allows users to select a location within the OneNote hierarchy structure.</span></span> <span data-ttu-id="77f3d-107">Las ubicaciones seleccionables incluyen los blocs de notas, grupos de sección, secciones, páginas y subpáginas.</span><span class="sxs-lookup"><span data-stu-id="77f3d-107">Selectable locations include notebooks, section groups, sections, pages, and subpages.</span></span> <span data-ttu-id="77f3d-108">El cuadro de diálogo se usa dentro de la aplicación de OneNote y por las aplicaciones externas a través de la API de OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="77f3d-108">The dialog box is used both within the OneNote application and by external applications through the OneNote 2013 API.</span></span> <span data-ttu-id="77f3d-109">La figura 1 muestra el cuadro de diálogo fiscal rápido en su estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="77f3d-109">Figure 1 shows the Quick Filing dialog box in its default state.</span></span>
  
<span data-ttu-id="77f3d-110">**En la figura 1. Cuadro de diálogo de archivado rápido sin personalizaciones**</span><span class="sxs-lookup"><span data-stu-id="77f3d-110">**Figure 1. Quick Filing dialog box without customizations**</span></span>

<span data-ttu-id="77f3d-111">![Cuadro de diálogo de archivado rápido sin personalizaciones] (media/ON15Con_quick_filing_dialog.jpg "Cuadro de diálogo de archivado rápido sin personalizaciones")</span><span class="sxs-lookup"><span data-stu-id="77f3d-111">![Quick Filing dialog box without customizations](media/ON15Con_quick_filing_dialog.jpg "Quick Filing dialog box without customizations")</span></span>
  
<span data-ttu-id="77f3d-112">En el cuadro de diálogo, los usuarios pueden navegar por la jerarquía de todos los blocs de notas para buscar ubicaciones específicas o buscar la estructura de árbol de OneNote escribiendo en el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="77f3d-112">Within the dialog box, users can navigate the All Notebooks hierarchy to look for specific locations or search the OneNote tree structure by typing into the text box.</span></span> <span data-ttu-id="77f3d-113">Aspectos del cuadro de diálogo que se pueden personalizar incluyen el título, descripción, lista de resultados de recientes, texto de la casilla de verificación y estado, profundidad de árbol, botones y tipos de ubicación seleccionable.</span><span class="sxs-lookup"><span data-stu-id="77f3d-113">Aspects of the dialog box that can be customized include the title, description, recent results list, check box text and state, tree depth, buttons, and selectable location types.</span></span>

<span data-ttu-id="77f3d-114">Puede tener acceso a la funcionalidad de cuadro de diálogo de archivado rápido a través de dos interfaces de OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="77f3d-114">You can access the Quick Filing dialog box functionality through two OneNote 2013 interfaces.</span></span> <span data-ttu-id="77f3d-115">La interfaz de **IQuickFilingDialog** permite a los usuarios crear instancias, configurar y ejecuta el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-115">The **IQuickFilingDialog** interface allows users to instantiate, set up, and run the dialog box.</span></span> <span data-ttu-id="77f3d-116">La interfaz de **IQuickFilingDialogCallback** se llama una vez que se cierra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-116">The **IQuickFilingDialogCallback** interface is called after the dialog box is closed.</span></span> <span data-ttu-id="77f3d-117">El cuadro de diálogo se ejecuta en el proceso de OneNote, por lo que se necesita un mecanismo para mantener los subprocesos del cuadro de diálogo Ejecutar y, a continuación, para capturar la selección del usuario y el estado del cuadro de diálogo cuando éste se cierra.</span><span class="sxs-lookup"><span data-stu-id="77f3d-117">The dialog box is run in the OneNote process, so a mechanism is needed to keep the dialog box's thread running and then to capture the user's selection and the state of the dialog box when it is closed.</span></span> 
  
## <a name="iquickfilingdialog-interface"></a><span data-ttu-id="77f3d-118">Interfaz IQuickFilingDialog</span><span class="sxs-lookup"><span data-stu-id="77f3d-118">IQuickFilingDialog interface</span></span>
<span data-ttu-id="77f3d-119"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="77f3d-119"></span></span>

<span data-ttu-id="77f3d-120">Esta interfaz permite al usuario personalizar y ejecutar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-120">This interface allows the user to customize and run the dialog box.</span></span> <span data-ttu-id="77f3d-121">El usuario puede crear una instancia de un cuadro de diálogo a través de la clase de **aplicación** mediante el método **Application.QuickFilingDialog** .</span><span class="sxs-lookup"><span data-stu-id="77f3d-121">The user can instantiate a dialog box through the **Application** class by using the **Application.QuickFilingDialog** method.</span></span> <span data-ttu-id="77f3d-122">El método devuelve una instancia del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-122">The method returns an instance of the dialog box.</span></span> <span data-ttu-id="77f3d-123">Una vez que se establecen las propiedades del cuadro de diálogo, el método **IQuickFilingDialog.Run** se usa para ejecutar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-123">Once the properties of the dialog box are set, the **IQuickFilingDialog.Run** method is used to run the dialog box.</span></span> <span data-ttu-id="77f3d-124">Este método ejecuta el cuadro de diálogo en un nuevo subproceso.</span><span class="sxs-lookup"><span data-stu-id="77f3d-124">This method runs the dialog box on a new thread.</span></span> 
  
<span data-ttu-id="77f3d-125">**Propiedades**</span><span class="sxs-lookup"><span data-stu-id="77f3d-125">**Properties**</span></span>

|<span data-ttu-id="77f3d-126">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="77f3d-126">**Name**</span></span>|<span data-ttu-id="77f3d-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="77f3d-127">**Type**</span></span>|<span data-ttu-id="77f3d-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77f3d-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="77f3d-129">**Title**</span><span class="sxs-lookup"><span data-stu-id="77f3d-129">**Title**</span></span> <br/> |<span data-ttu-id="77f3d-130">string</span><span class="sxs-lookup"><span data-stu-id="77f3d-130">string</span></span>  <br/> |<span data-ttu-id="77f3d-131">Obtiene o establece el texto del título que aparece en la barra de título de la ventana del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-131">Gets or sets the title text that appears in the title bar of the dialog box window.</span></span>  <br/> |
|<span data-ttu-id="77f3d-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77f3d-132">**Description**</span></span> <br/> |<span data-ttu-id="77f3d-133">string</span><span class="sxs-lookup"><span data-stu-id="77f3d-133">string</span></span>  <br/> |<span data-ttu-id="77f3d-134">Obtiene o establece la descripción de texto para indicar al usuario acerca de lo que seleccione.</span><span class="sxs-lookup"><span data-stu-id="77f3d-134">Gets or sets the text description to instruct the user about what to select.</span></span> <span data-ttu-id="77f3d-135">Este valor puede ser texto con varias líneas.</span><span class="sxs-lookup"><span data-stu-id="77f3d-135">This value can be multiple-line text.</span></span>  <br/> |
|<span data-ttu-id="77f3d-136">**CheckboxText**</span><span class="sxs-lookup"><span data-stu-id="77f3d-136">**CheckboxText**</span></span> <br/> |<span data-ttu-id="77f3d-137">string</span><span class="sxs-lookup"><span data-stu-id="77f3d-137">string</span></span>  <br/> |<span data-ttu-id="77f3d-138">Obtiene o establece el texto que sigue a la casilla de verificación.</span><span class="sxs-lookup"><span data-stu-id="77f3d-138">Gets or sets the text that follows the check box.</span></span> <span data-ttu-id="77f3d-139">Si este valor se establece en una cadena no vacía, aparece una casilla de verificación en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-139">If this value is set to a non-empty string, a check box appears in the dialog box.</span></span> <span data-ttu-id="77f3d-140">Si el valor es una cadena vacía, no aparece ningún cuadro de verificación.</span><span class="sxs-lookup"><span data-stu-id="77f3d-140">If the value is an empty string, no check box appears.</span></span>  <br/> |
|<span data-ttu-id="77f3d-141">**CheckboxState**</span><span class="sxs-lookup"><span data-stu-id="77f3d-141">**CheckboxState**</span></span> <br/> |<span data-ttu-id="77f3d-142">bool</span><span class="sxs-lookup"><span data-stu-id="77f3d-142">bool</span></span>  <br/> |<span data-ttu-id="77f3d-143">Obtiene o establece el estado de la casilla de verificación.</span><span class="sxs-lookup"><span data-stu-id="77f3d-143">Gets or sets the state of the check box.</span></span> <span data-ttu-id="77f3d-144">Si el valor se establece en **false**, la casilla de verificación está desactivada cuando se inicia el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-144">If value is set to **false**, the check box is cleared when the dialog box is started.</span></span> <span data-ttu-id="77f3d-145">Si el valor se establece en **true**, se selecciona la casilla de verificación cuando el cuadro de diálogo se inicia mientras **CheckboxText** es una cadena no vacía.</span><span class="sxs-lookup"><span data-stu-id="77f3d-145">If the value is set to **true**, the check box is selected when the dialog box is started as long as **CheckboxText** is a non-empty string.</span></span>  <br/> |
|<span data-ttu-id="77f3d-146">**WindowHandle**</span><span class="sxs-lookup"><span data-stu-id="77f3d-146">**WindowHandle**</span></span> <br/> |<span data-ttu-id="77f3d-147">ulong</span><span class="sxs-lookup"><span data-stu-id="77f3d-147">ulong</span></span>  <br/> |<span data-ttu-id="77f3d-148">Obtiene el identificador del controlador de la ventana de cuadro de diálogo de archivado rápido.</span><span class="sxs-lookup"><span data-stu-id="77f3d-148">Gets the handle ID of the Quick Filing dialog box window.</span></span>  <br/> |
|<span data-ttu-id="77f3d-149">**TreeDepth**</span><span class="sxs-lookup"><span data-stu-id="77f3d-149">**TreeDepth**</span></span> <br/> |<span data-ttu-id="77f3d-150">**HierarchyElement**</span><span class="sxs-lookup"><span data-stu-id="77f3d-150">**HierarchyElement**</span></span> <br/> |<span data-ttu-id="77f3d-151">Obtiene o establece la profundidad, el árbol de OneNote debe mostrarse en la sección de todos los blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="77f3d-151">Gets or sets how deep the OneNote tree should be displayed in the All Notebooks section.</span></span> <span data-ttu-id="77f3d-152">De forma predeterminada, se muestra el árbol hasta las secciones.</span><span class="sxs-lookup"><span data-stu-id="77f3d-152">By default, the tree is displayed up to the sections.</span></span> <span data-ttu-id="77f3d-153">Esta propiedad no afecta a qué tipo de elementos que se puede seleccionar.</span><span class="sxs-lookup"><span data-stu-id="77f3d-153">This property does not affect what type of elements can be selected.</span></span>  <br/> <span data-ttu-id="77f3d-154">Si **TreeDepth** se establece en un elemento inferior en la jerarquía de OneNote que se puede seleccionar cualquiera de los botones, la profundidad de árbol que se muestra será el elemento seleccionable posible más bajo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-154">If **TreeDepth** is set to an element lower in the OneNote hierarchy than can be selected by any of the buttons, the displayed tree depth will be the lowest possible selectable element.</span></span> <span data-ttu-id="77f3d-155">Es decir, si se establece la profundidad de árbol para mostrar hacia abajo hasta las páginas, pero el elemento seleccionable más bajo es una sección, se muestra el árbol hacia abajo hasta secciones.</span><span class="sxs-lookup"><span data-stu-id="77f3d-155">That is, if tree depth is set to display down to pages, but the lowest selectable element is a section, the tree is displayed down to sections.</span></span>  <br/> |
|<span data-ttu-id="77f3d-156">**ParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="77f3d-156">**ParentWindowHandle**</span></span> <br/> |<span data-ttu-id="77f3d-157">ulong</span><span class="sxs-lookup"><span data-stu-id="77f3d-157">ulong</span></span>  <br/> |<span data-ttu-id="77f3d-158">Obtiene o establece el identificador del controlador de la ventana principal del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-158">Gets or sets the handle ID of the parent window of the dialog box.</span></span> <span data-ttu-id="77f3d-159">Si se establece esta propiedad, el cuadro de diálogo fiscal rápido será modal a la ventana primaria asignado cuando se abre el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-159">If this property is set, the Quick Filing dialog box will be modal to the assigned parent window when the dialog box opens.</span></span> <span data-ttu-id="77f3d-160">Es decir, un usuario no podrá tener acceso a la ventana principal hasta que se cierre el cuadro de diálogo de archivado rápido.</span><span class="sxs-lookup"><span data-stu-id="77f3d-160">That is, a user will not be able to access the parent window until the Quick Filing dialog box is closed.</span></span>  <br/> |
|<span data-ttu-id="77f3d-161">**Position**</span><span class="sxs-lookup"><span data-stu-id="77f3d-161">**Position**</span></span> <br/> |<span data-ttu-id="77f3d-162">tagPOINT</span><span class="sxs-lookup"><span data-stu-id="77f3d-162">tagPOINT</span></span>  <br/> |<span data-ttu-id="77f3d-163">Obtiene o establece la posición de la ventana en relación con la pantalla.</span><span class="sxs-lookup"><span data-stu-id="77f3d-163">Gets or sets the position of the window in relation to the screen.</span></span> <span data-ttu-id="77f3d-164">De forma predeterminada, el cuadro de diálogo aparece en medio de la ventana principal o el escritorio.</span><span class="sxs-lookup"><span data-stu-id="77f3d-164">By default, the dialog box appears in the middle of the parent window or the desktop.</span></span>  <br/> |
|<span data-ttu-id="77f3d-165">**SelectedItem**</span><span class="sxs-lookup"><span data-stu-id="77f3d-165">**SelectedItem**</span></span> <br/> |<span data-ttu-id="77f3d-166">string</span><span class="sxs-lookup"><span data-stu-id="77f3d-166">string</span></span>  <br/> |<span data-ttu-id="77f3d-167">Obtiene el identificador del objeto de la ubicación de OneNote seleccionado por el usuario cuando se cierra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-167">Gets the object ID of the OneNote location selected by the user when the dialog box is closed.</span></span> <span data-ttu-id="77f3d-168">Si el usuario hace clic en el botón **Cancelar** , el objeto se establece en null.</span><span class="sxs-lookup"><span data-stu-id="77f3d-168">If the user clicks the **Cancel** button, the object is set to null.</span></span>  <br/> |
|<span data-ttu-id="77f3d-169">**PressedButton**</span><span class="sxs-lookup"><span data-stu-id="77f3d-169">**PressedButton**</span></span> <br/> |<span data-ttu-id="77f3d-170">ulong</span><span class="sxs-lookup"><span data-stu-id="77f3d-170">ulong</span></span>  <br/> |<span data-ttu-id="77f3d-171">Obtiene qué botón se hizo clic cuando se ha cerrado el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-171">Gets which button was clicked when the dialog box was closed.</span></span> <span data-ttu-id="77f3d-172">Si se ha hecho clic en el botón **Cancelar** , esta propiedad devuelve un valor de -1.</span><span class="sxs-lookup"><span data-stu-id="77f3d-172">If the **Cancel** button was clicked, this property returns a value of -1.</span></span> <span data-ttu-id="77f3d-173">Todos los otros botones se asignan valores enteros del 0, incrementada en 1 para cada botón que agregó en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-173">All other buttons are assigned integer values from 0, incremented by 1 for each button added to the dialog box.</span></span> <span data-ttu-id="77f3d-174">El valor de número entero del botón **Aceptar** predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="77f3d-174">The integer value of the default **OK** button is 0.</span></span>  <br/> |
   
### <a name="methods"></a><span data-ttu-id="77f3d-175">Métodos</span><span class="sxs-lookup"><span data-stu-id="77f3d-175">Methods</span></span>

<span data-ttu-id="77f3d-176">**SetRecentResults**</span><span class="sxs-lookup"><span data-stu-id="77f3d-176">**SetRecentResults**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77f3d-177">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77f3d-177">**Description**</span></span> <br/> |<span data-ttu-id="77f3d-178">Establece qué lista resultado recientes se mostrará en el cuadro de diálogo fiscal rápido e indica si se incluyen algunas ubicaciones de presentación especial en la lista.</span><span class="sxs-lookup"><span data-stu-id="77f3d-178">Sets what recent result list will be displayed in the Quick Filing dialog box, and indicates whether to include some special filing locations in the list.</span></span> <span data-ttu-id="77f3d-179">Los usuarios pueden seleccionar una lista de resultados recientes de la enumeración [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) .</span><span class="sxs-lookup"><span data-stu-id="77f3d-179">Users can select a recent result list from the [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) enumeration.</span></span> <span data-ttu-id="77f3d-180">Los usuarios también pueden elegir agregar las siguientes opciones a la lista: sección actual, la página actual o notas sin archivar.</span><span class="sxs-lookup"><span data-stu-id="77f3d-180">Users can also choose to add the following options to the list: Current Section, Current Page, or Unfiled Notes.</span></span> <span data-ttu-id="77f3d-181">Si se selecciona **RecentResultType.rrtNone** , no se muestra ninguna lista de resultados recientes.</span><span class="sxs-lookup"><span data-stu-id="77f3d-181">If **RecentResultType.rrtNone** is selected, no recent result list is shown.</span></span>  <br/> |
|<span data-ttu-id="77f3d-182">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="77f3d-182">**Syntax**</span></span> <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|<span data-ttu-id="77f3d-183">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="77f3d-183">**Parameters**</span></span> <br/> | <span data-ttu-id="77f3d-184">_recentResults_ &ndash; Un objeto de tipo **RecentResultType** que indica qué lista resultado reciente, si lo hay, debe aparecer.</span><span class="sxs-lookup"><span data-stu-id="77f3d-184">_recentResults_ &ndash; An object of type **RecentResultType** that indicates which recent result list, if any, should appear.</span></span> <span data-ttu-id="77f3d-185">Si se selecciona **rrtNone** , no aparecerá ninguna lista de resultados recientes en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-185">If **rrtNone** is selected, no recent result list appears in the dialog box.</span></span><br/><br/>  <span data-ttu-id="77f3d-186">_fShowCurrentSection_ &ndash; Valor de tipo Boolean que indica si la sección actual debe estar incluida en la lista de resultados recientes.</span><span class="sxs-lookup"><span data-stu-id="77f3d-186">_fShowCurrentSection_ &ndash; A Boolean value that indicates whether the current section should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="77f3d-187">_fShowCurrentPage_ &ndash; Valor de tipo Boolean que indica si la página actual debe estar incluida en la lista de resultados recientes.</span><span class="sxs-lookup"><span data-stu-id="77f3d-187">_fShowCurrentPage_ &ndash; A Boolean value that indicates whether the current page should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="77f3d-188">_fShowUnfiledNotes_ &ndash; Valor de tipo Boolean que indica si la sección Notas sin archivar debe estar incluida en la lista de resultados recientes.</span><span class="sxs-lookup"><span data-stu-id="77f3d-188">_fShowUnfiledNotes_ &ndash; A Boolean value that indicates whether the Unfiled Notes section should be included in the recent result list.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="77f3d-189">Si no se puede seleccionar una ubicación de archivado especiales mediante cualquiera de los botones en el cuadro de diálogo, no se muestra en la lista.</span><span class="sxs-lookup"><span data-stu-id="77f3d-189">If a special filing location cannot be selected by using any of the buttons in the dialog box, it is not shown in the list.</span></span> <span data-ttu-id="77f3d-190">Si no hay ningún elemento seleccionable en la lista de resultados recientes se encuentra, no se muestra ninguna lista de resultados recientes.</span><span class="sxs-lookup"><span data-stu-id="77f3d-190">If no selectable item in the recent results list is found, no recent result list is displayed.</span></span> 
  
<span data-ttu-id="77f3d-191">En el siguiente ejemplo, se utiliza el método **SetRecentResults** para mostrar la sección actual, la página actual y la sección Notas sin archivar en la lista de resultados recientes.</span><span class="sxs-lookup"><span data-stu-id="77f3d-191">The following example uses the **SetRecentResults** method to display the current section, current page, and the Unfiled Notes section in the recent result list.</span></span> 
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            ...
        }

```

<span data-ttu-id="77f3d-192">**Botón Agregar**</span><span class="sxs-lookup"><span data-stu-id="77f3d-192">**AddButton**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77f3d-193">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77f3d-193">**Description**</span></span> <br/> |<span data-ttu-id="77f3d-194">Permite a los usuarios agregar y personalizar los botones en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-194">Allows users to add and customize buttons in the dialog box.</span></span> <span data-ttu-id="77f3d-195">Los usuarios pueden especificar el texto en los botones y se pueden seleccionar qué elementos de la jerarquía de OneNote por cada botón.</span><span class="sxs-lookup"><span data-stu-id="77f3d-195">Users can specify the text on the buttons and what elements of the OneNote hierarchy can be selected by each button.</span></span>  <br/> |
|<span data-ttu-id="77f3d-196">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="77f3d-196">**Syntax**</span></span> <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|<span data-ttu-id="77f3d-197">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="77f3d-197">**Parameters**</span></span> <br/> | <span data-ttu-id="77f3d-198">_bstrText_ &ndash; Una cadena que especifica el texto para que aparezca en el botón.</span><span class="sxs-lookup"><span data-stu-id="77f3d-198">_bstrText_ &ndash; A string that specifies the text to appear on the button.</span></span> <span data-ttu-id="77f3d-199">Para personalizar el botón **Aceptar** de forma predeterminada, pase un valor null como **bstrText**.</span><span class="sxs-lookup"><span data-stu-id="77f3d-199">To customize the default **OK** button, pass in a null value as **bstrText**.</span></span>  <br/><br/><span data-ttu-id="77f3d-200">_allowedElements_ &ndash; Un **HierarchyElement** que indica qué elementos de jerarquía de OneNote que no sean de solo lectura que se permite un usuario para seleccionar mediante el botón.</span><span class="sxs-lookup"><span data-stu-id="77f3d-200">_allowedElements_ &ndash; A **HierarchyElement** that indicates what non-read-only OneNote hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="77f3d-201">Para seleccionar varios elementos, el usuario debe pasar el operador **OR** para todos los valores de uint al equivalente de los tipos de **HierarchyElement** permitidos como un **HierarchyElement**.</span><span class="sxs-lookup"><span data-stu-id="77f3d-201">For selecting multiple items, the user should pass in the **OR** operator for all the uint equivalent values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="77f3d-202">_allowedReadOnlyElements_ &ndash; Un **HierarchyElement** que indica qué elementos de la jerarquía de solo lectura de OneNote que se permite un usuario para seleccionar mediante el botón.</span><span class="sxs-lookup"><span data-stu-id="77f3d-202">_allowedReadOnlyElements_ &ndash; A **HierarchyElement** that indicates what OneNote read-only hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="77f3d-203">Para seleccionar varios elementos, el usuario debe pasar el operador **OR** para todos los valores de los tipos de **HierarchyElement** permitidos como un **HierarchyElement**equivalentes de **uint** .</span><span class="sxs-lookup"><span data-stu-id="77f3d-203">For selecting multiple items, the user should pass in the **OR** operator for all the **uint** equivalents values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="77f3d-204">_fDefault_ &ndash; Valor de tipo Boolean que especifica si este botón debe ser el botón predeterminado.</span><span class="sxs-lookup"><span data-stu-id="77f3d-204">_fDefault_ &ndash; A Boolean value that specifies whether this button should be the default button.</span></span> <span data-ttu-id="77f3d-205">Si se establecen varios botones como predeterminada, el último botón especificado se convierte en el botón predeterminado.</span><span class="sxs-lookup"><span data-stu-id="77f3d-205">If multiple buttons are set as default, the last specified button becomes the default button.</span></span>  <br/> |
   
<span data-ttu-id="77f3d-206">En el siguiente ejemplo agrega tres botones en el cuadro de diálogo de archivado rápido.</span><span class="sxs-lookup"><span data-stu-id="77f3d-206">The following example adds three buttons to the Quick Filing dialog box.</span></span> <span data-ttu-id="77f3d-207">El primero de ellos, **todos los**, se puede seleccionar por todos los elementos en el árbol de la jerarquía de OneNote.</span><span class="sxs-lookup"><span data-stu-id="77f3d-207">The first one, **All**, can be selected by all elements in the OneNote hierarchy tree.</span></span> <span data-ttu-id="77f3d-208">Los demás, **los blocs de notas** y **las páginas**, pueden seleccionar sólo si sus elementos correspondientes, los blocs de notas y las páginas, se seleccionan.</span><span class="sxs-lookup"><span data-stu-id="77f3d-208">The others, **Notebooks** and **Pages**, can be selected only if their corresponding elements, Notebooks and Pages, are selected.</span></span>
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            ... 
        }

```

<span data-ttu-id="77f3d-209">**Run**</span><span class="sxs-lookup"><span data-stu-id="77f3d-209">**Run**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77f3d-210">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77f3d-210">**Description**</span></span> <br/> |<span data-ttu-id="77f3d-211">Muestra el cuadro de diálogo de archivado rápido desde un subproceso nuevo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-211">Displays the Quick Filing dialog box from a new thread.</span></span> <span data-ttu-id="77f3d-212">Toma una referencia a la interfaz **IQuickFilingDialogCallback** , cuyo **OnDialogClosed** llamará al método una vez que se cierra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-212">It takes a reference to the **IQuickFilingDialogCallback** interface, whose **OnDialogClosed** method will be called once the dialog box closes.</span></span>  <br/> |
|<span data-ttu-id="77f3d-213">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="77f3d-213">**Syntax**</span></span> <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|<span data-ttu-id="77f3d-214">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="77f3d-214">**Parameters**</span></span> <br/> | <span data-ttu-id="77f3d-215">_piCallback_ &ndash; Una referencia a la interfaz de **IQuickFilingDialogCallback** que se creará una instancia una vez que se cierra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-215">_piCallback_ &ndash; A reference to the **IQuickFilingDialogCallback** interface that will be instantiated once the dialog box closes.</span></span>  <br/> |
   
<span data-ttu-id="77f3d-216">En el ejemplo siguiente se usa el método **Run** para mostrar el cuadro de diálogo de archivado rápido desde un subproceso nuevo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-216">The following example uses the **Run** method to display the Quick Filing dialog box from a new thread.</span></span> 
  
```cs
    class OpenQuickFilingDialog
    {
            ... 
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            ... 
        }
    }

```

<span data-ttu-id="77f3d-217">**TreeCollapsedState**</span><span class="sxs-lookup"><span data-stu-id="77f3d-217">**TreeCollapsedState**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77f3d-218">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77f3d-218">**Description**</span></span> <br/> |<span data-ttu-id="77f3d-219">Indica si se debe expandir o contraer el árbol de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="77f3d-219">Indicates whether the hierarchy tree should be expanded or collapsed.</span></span>  <br/> |
|<span data-ttu-id="77f3d-220">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="77f3d-220">**Syntax**</span></span> <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|<span data-ttu-id="77f3d-221">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="77f3d-221">**Parameters**</span></span> <br/> | <span data-ttu-id="77f3d-222">_tcs_ - especifica si el árbol está expandido o contraído.</span><span class="sxs-lookup"><span data-stu-id="77f3d-222">_tcs_ - Specifies whether the tree is expanded or collapsed.</span></span>  <br/> |
   
<span data-ttu-id="77f3d-223">**NotebookFilterOut**</span><span class="sxs-lookup"><span data-stu-id="77f3d-223">**NotebookFilterOut**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77f3d-224">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77f3d-224">**Description**</span></span> <br/> |<span data-ttu-id="77f3d-225">Filtra la lista de blocs de notas que se muestran por tipo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-225">Filters the list of notebooks shown by type.</span></span>  <br/> |
|<span data-ttu-id="77f3d-226">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="77f3d-226">**Syntax**</span></span> <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|<span data-ttu-id="77f3d-227">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="77f3d-227">**Parameters**</span></span> <br/> | <span data-ttu-id="77f3d-228">_nfo_ - especifica el conjunto de los blocs de notas que se deben filtrar fuera de la lista</span><span class="sxs-lookup"><span data-stu-id="77f3d-228">_nfo_ - Specifies the set of notebooks that are to be filtered out of the list</span></span>  <br/> |
   
<span data-ttu-id="77f3d-229">**ShowCreateNewNotebook**</span><span class="sxs-lookup"><span data-stu-id="77f3d-229">**ShowCreateNewNotebook**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77f3d-230">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77f3d-230">**Description**</span></span> <br/> |<span data-ttu-id="77f3d-231">Muestra la opción Crear nuevo bloc de notas en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-231">Displays the create new notebook option in the dialog.</span></span>  <br/> |
|<span data-ttu-id="77f3d-232">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="77f3d-232">**Syntax**</span></span> <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|<span data-ttu-id="77f3d-233">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="77f3d-233">**Parameters**</span></span> <br/> |<span data-ttu-id="77f3d-234">Ninguno</span><span class="sxs-lookup"><span data-stu-id="77f3d-234">None</span></span>  <br/> |
   
<span data-ttu-id="77f3d-235">**AddInitialEditor**</span><span class="sxs-lookup"><span data-stu-id="77f3d-235">**AddInitialEditor**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77f3d-236">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77f3d-236">**Description**</span></span> <br/> |<span data-ttu-id="77f3d-237">Agrega un usuario como un editor inicial en un bloc de notas en el cuadro de diálogo de archivado rápido.</span><span class="sxs-lookup"><span data-stu-id="77f3d-237">Adds a user as an initial editor to a notebook in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="77f3d-238">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="77f3d-238">**Syntax**</span></span> <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|<span data-ttu-id="77f3d-239">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="77f3d-239">**Parameters**</span></span> <br/> | <span data-ttu-id="77f3d-240">_initialEditor_ - la dirección de correo electrónico del usuario que desea agregar como un editor en el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="77f3d-240">_initialEditor_ - The email address of the user you wish to add as an editor to the notebook.</span></span> <span data-ttu-id="77f3d-241">Cuando se crea el Bloc de notas mediante el cuadro de diálogo fiscal rápida, se comparte automáticamente con todos los editores inicial.</span><span class="sxs-lookup"><span data-stu-id="77f3d-241">When the notebook is created via the Quick Filing dialog box, it is automatically shared with all Initial Editors.</span></span>  <br/> |
   
<span data-ttu-id="77f3d-242">**ClearInitialEditors**</span><span class="sxs-lookup"><span data-stu-id="77f3d-242">**ClearInitialEditors**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77f3d-243">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77f3d-243">**Description**</span></span> <br/> |<span data-ttu-id="77f3d-244">Quita todos los editores iniciales desde el cuadro de diálogo de archivado rápido.</span><span class="sxs-lookup"><span data-stu-id="77f3d-244">Removes all initial editors from the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="77f3d-245">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="77f3d-245">**Syntax**</span></span> <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|<span data-ttu-id="77f3d-246">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="77f3d-246">**Parameters**</span></span> <br/> |<span data-ttu-id="77f3d-247">Ninguno</span><span class="sxs-lookup"><span data-stu-id="77f3d-247">None</span></span>  <br/> |
   
<span data-ttu-id="77f3d-248">**ShowSharingHyperlink**</span><span class="sxs-lookup"><span data-stu-id="77f3d-248">**ShowSharingHyperlink**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77f3d-249">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77f3d-249">**Description**</span></span> <br/> |<span data-ttu-id="77f3d-250">Muestra el hipervínculo del tema de Ayuda de uso compartido en el cuadro de diálogo de archivado rápido.</span><span class="sxs-lookup"><span data-stu-id="77f3d-250">Displays the Sharing Help Topic Hyperlink in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="77f3d-251">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="77f3d-251">**Syntax**</span></span> <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|<span data-ttu-id="77f3d-252">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="77f3d-252">**Parameters**</span></span> <br/> |<span data-ttu-id="77f3d-253">Ninguno</span><span class="sxs-lookup"><span data-stu-id="77f3d-253">None</span></span>  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a><span data-ttu-id="77f3d-254">Interfaz IQuickFilingDialogCallback</span><span class="sxs-lookup"><span data-stu-id="77f3d-254">IQuickFilingDialogCallback interface</span></span>
<span data-ttu-id="77f3d-255"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="77f3d-255"></span></span>

<span data-ttu-id="77f3d-256">Esta interfaz permite al usuario tener acceso a las propiedades del cuadro de diálogo cuando se cierra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-256">This interface allows the user to access the dialog box properties after the dialog box closes.</span></span> <span data-ttu-id="77f3d-257">Una vez que se cierra el cuadro de diálogo, OneNote 2013 llama al método de **IQuickFilingDialogCallback.OnDialogClose** en esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="77f3d-257">Once the dialog box closes, OneNote 2013 calls the **IQuickFilingDialogCallback.OnDialogClose** method in this interface.</span></span> 
  
<span data-ttu-id="77f3d-258">Una clase que hereda esta interfaz debe estar definido.</span><span class="sxs-lookup"><span data-stu-id="77f3d-258">A class that inherits this interface has to be defined.</span></span>
  
### <a name="methods"></a><span data-ttu-id="77f3d-259">Métodos</span><span class="sxs-lookup"><span data-stu-id="77f3d-259">Methods</span></span>

<span data-ttu-id="77f3d-260">En la siguiente sección se describe los métodos asociados con las interfaces detalladas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="77f3d-260">The following section describes the methods associated with the interfaces detailed previously.</span></span>
  
<span data-ttu-id="77f3d-261">**OnDialogClosed**</span><span class="sxs-lookup"><span data-stu-id="77f3d-261">**OnDialogClosed**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77f3d-262">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77f3d-262">**Description**</span></span> <br/> |<span data-ttu-id="77f3d-263">Permite a los usuarios agregar la funcionalidad para capturar y utilizar la selección del usuario desde el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-263">Enables users to add functionality to capture and use the user selection from the dialog box.</span></span> <span data-ttu-id="77f3d-264">Se llama a este método después de cerrar el cuadro de diálogo de archivado rápido.</span><span class="sxs-lookup"><span data-stu-id="77f3d-264">This method is called after the Quick Filing dialog box is closed.</span></span> <span data-ttu-id="77f3d-265">Este método es una función que tienen interfaces de **IQuickFilingDialogCallback** para definir.</span><span class="sxs-lookup"><span data-stu-id="77f3d-265">This method is a function that **IQuickFilingDialogCallback** interfaces have to define.</span></span>  <br/> |
|<span data-ttu-id="77f3d-266">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="77f3d-266">**Syntax**</span></span> <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|<span data-ttu-id="77f3d-267">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="77f3d-267">**Parameters**</span></span> <br/> | <span data-ttu-id="77f3d-268">_cuadro de diálogo_ &ndash; El objeto **IQuickFilingDialog** que llamó al método **OnDialogClose** .</span><span class="sxs-lookup"><span data-stu-id="77f3d-268">_dialog_ &ndash; The **IQuickFilingDialog** object that called the **OnDialogClose** method.</span></span>  <br/> |
   
<span data-ttu-id="77f3d-269">El ejemplo siguiente es una interfaz de **IQuickFilingDialogCallback** de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-269">The following example is a sample **IQuickFilingDialogCallback** interface.</span></span> <span data-ttu-id="77f3d-270">El método **OnDialogClose** imprime la selección del usuario desde el cuadro de diálogo fiscal rápido en la consola.</span><span class="sxs-lookup"><span data-stu-id="77f3d-270">The **OnDialogClose** method prints the user's selection from the Quick Filing dialog box to the console.</span></span> 
  
```cs
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }

```

## <a name="example"></a><span data-ttu-id="77f3d-271">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="77f3d-271">Example</span></span>
<span data-ttu-id="77f3d-272"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="77f3d-272"></span></span>

<span data-ttu-id="77f3d-273">En el ejemplo de código siguiente se abre un cuadro de diálogo de archivado rápido que tiene un título personalizado, descripción, lista de resultados recientes, profundidad de árbol, casilla de verificación y los botones.</span><span class="sxs-lookup"><span data-stu-id="77f3d-273">The following code example opens a Quick Filing dialog box that has a customized title, description, recent result list, tree depth, check box, and buttons.</span></span> <span data-ttu-id="77f3d-274">El usuario seleccionado el elemento, que se ha presionado el botón, y el estado de la casilla de verificación se mostrará en una ventana de la consola cuando se cierra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="77f3d-274">The user's selected item, pressed button, and check-box state will be displayed in a console window when the dialog box is closed.</span></span> <span data-ttu-id="77f3d-275">Para ver el botón de página habilitado, el usuario tendrá que buscar una página y selecciónelo, debido a que se establece la profundidad de árbol hacia abajo a las secciones.</span><span class="sxs-lookup"><span data-stu-id="77f3d-275">To see the page button enabled, the user will have to search for a page and select it, because the tree depth is set down to sections.</span></span> <span data-ttu-id="77f3d-276">El cuadro de diálogo no es un elemento secundario de cualquier ventana.</span><span class="sxs-lookup"><span data-stu-id="77f3d-276">The dialog box is not a child of any window.</span></span>
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using Microsoft.Office.Interop.OneNote;
namespace SampleQFD
{
    class OpenQuickFilingDialog
    {
        private static EventWaitHandle wh = new AutoResetEvent(false);
        private static IQuickFilingDialog qfDialog;
        private static String strTitle = "Sample Title";
        private static String strDescription = "Sample Description";
        private static String strCheckboxText = "Sample Checkbox";
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            // Instantiate Quick Filing UI
            qfDialog = app.QuickFiling();
            #region//SET API PARAMETERS
            // TITLE
            qfDialog.Title = strTitle;
            // DESCRIPTION
            qfDialog.Description = strDescription;
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            // TREE DEPTH
            qfDialog.TreeDepth = HierarchyElement.heSections;
            // CHECKBOX
            qfDialog.CheckboxText = strCheckboxText;
            qfDialog.CheckboxState = false;
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            // PARENTWINDOW
            #endregion
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            // Clean up and Wait so console window does not close
            qfDialog = null;
            wh.WaitOne();
        }
    }
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }
}

```

## <a name="see-also"></a><span data-ttu-id="77f3d-277">Vea también</span><span class="sxs-lookup"><span data-stu-id="77f3d-277">See also</span></span>

- [<span data-ttu-id="77f3d-278">Referencia para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="77f3d-278">OneNote developer reference</span></span>](onenote-developer-reference.md)

