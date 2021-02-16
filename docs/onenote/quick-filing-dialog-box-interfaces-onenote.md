---
title: Interfaces de cuadro de diálogo de archivado rápido (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: En este tema se describen las interfaces que puede usar para personalizar mediante programación el cuadro de diálogo Archivado rápido en OneNote 2013.
ms.openlocfilehash: dd6b28ae6cb2acb007bae26ea661facaf1f8d4be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425340"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a><span data-ttu-id="6f8a1-103">Interfaces de cuadro de diálogo de archivado rápido (OneNote)</span><span class="sxs-lookup"><span data-stu-id="6f8a1-103">Quick Filing dialog box interfaces (OneNote)</span></span>

<span data-ttu-id="6f8a1-104">En este tema se describen las interfaces que puede usar para personalizar mediante programación el cuadro de diálogo Archivado rápido en OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-104">This topic describes the interfaces that you can use to programmatically customize the Quick Filing dialog box in OneNote 2013.</span></span>
  
## <a name="quick-filing-dialog-box"></a><span data-ttu-id="6f8a1-105">Cuadro de diálogo Archivado rápido</span><span class="sxs-lookup"><span data-stu-id="6f8a1-105">Quick Filing dialog box</span></span>

<span data-ttu-id="6f8a1-106">El cuadro de diálogo Archivado rápido de OneNote 2013 es un cuadro de diálogo personalizable que permite a los usuarios seleccionar una ubicación dentro de la estructura jerárquica de OneNote.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-106">The Quick Filing dialog box in OneNote 2013 is a customizable dialog box that allows users to select a location within the OneNote hierarchy structure.</span></span> <span data-ttu-id="6f8a1-107">Las ubicaciones seleccionables incluyen blocs de notas, grupos de secciones, secciones, páginas y subpáginas.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-107">Selectable locations include notebooks, section groups, sections, pages, and subpages.</span></span> <span data-ttu-id="6f8a1-108">El cuadro de diálogo se usa tanto en la aplicación de OneNote como en aplicaciones externas a través de la API de OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-108">The dialog box is used both within the OneNote application and by external applications through the OneNote 2013 API.</span></span> <span data-ttu-id="6f8a1-109">La figura 1 muestra el cuadro de diálogo Archivado rápido en su estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-109">Figure 1 shows the Quick Filing dialog box in its default state.</span></span>
  
<span data-ttu-id="6f8a1-110">**Figura 1. Cuadro de diálogo Archivado rápido sin personalizaciones**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-110">**Figure 1. Quick Filing dialog box without customizations**</span></span>

<span data-ttu-id="6f8a1-111">![Cuadro de diálogo Archivado rápido sin personalizaciones]Cuadro de diálogo(media/ON15Con_quick_filing_dialog.jpg "Archivado rápido sin personalizaciones")</span><span class="sxs-lookup"><span data-stu-id="6f8a1-111">![Quick Filing dialog box without customizations](media/ON15Con_quick_filing_dialog.jpg "Quick Filing dialog box without customizations")</span></span>
  
<span data-ttu-id="6f8a1-112">En el cuadro de diálogo, los usuarios pueden navegar por la jerarquía Todos los blocs de notas para buscar ubicaciones específicas o buscar en la estructura de árbol de OneNote escribiendo en el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-112">Within the dialog box, users can navigate the All Notebooks hierarchy to look for specific locations or search the OneNote tree structure by typing into the text box.</span></span> <span data-ttu-id="6f8a1-113">Entre los aspectos del cuadro de diálogo que se pueden personalizar se incluyen el título, la descripción, la lista de resultados recientes, el texto y el estado de la casilla de verificación, la profundidad del árbol, los botones y los tipos de ubicación seleccionables.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-113">Aspects of the dialog box that can be customized include the title, description, recent results list, check box text and state, tree depth, buttons, and selectable location types.</span></span>

<span data-ttu-id="6f8a1-114">Puede acceder a la funcionalidad del cuadro de diálogo Archivado rápido a través de dos interfaces de OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-114">You can access the Quick Filing dialog box functionality through two OneNote 2013 interfaces.</span></span> <span data-ttu-id="6f8a1-115">La **interfaz IQuickFilingDialog** permite a los usuarios crear instancias, configurar y ejecutar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-115">The **IQuickFilingDialog** interface allows users to instantiate, set up, and run the dialog box.</span></span> <span data-ttu-id="6f8a1-116">Se llama a la interfaz **IQuickFilingDialogCallback** después de cerrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-116">The **IQuickFilingDialogCallback** interface is called after the dialog box is closed.</span></span> <span data-ttu-id="6f8a1-117">El cuadro de diálogo se ejecuta en el proceso de OneNote, por lo que se necesita un mecanismo para mantener el subproceso del cuadro de diálogo en ejecución y, a continuación, capturar la selección del usuario y el estado del cuadro de diálogo cuando se cierra.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-117">The dialog box is run in the OneNote process, so a mechanism is needed to keep the dialog box's thread running and then to capture the user's selection and the state of the dialog box when it is closed.</span></span> 
  
## <a name="iquickfilingdialog-interface"></a><span data-ttu-id="6f8a1-118">Interfaz IQuickFilingDialog</span><span class="sxs-lookup"><span data-stu-id="6f8a1-118">IQuickFilingDialog interface</span></span>
<span data-ttu-id="6f8a1-119"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="6f8a1-119"><a name="odc_IQuickFilingDialog"> </a></span></span>

<span data-ttu-id="6f8a1-120">Esta interfaz permite al usuario personalizar y ejecutar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-120">This interface allows the user to customize and run the dialog box.</span></span> <span data-ttu-id="6f8a1-121">El usuario puede crear una instancia de un cuadro de diálogo a través de la **clase Application** mediante el método **Application.QuickFilingDialog** .</span><span class="sxs-lookup"><span data-stu-id="6f8a1-121">The user can instantiate a dialog box through the **Application** class by using the **Application.QuickFilingDialog** method.</span></span> <span data-ttu-id="6f8a1-122">El método devuelve una instancia del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-122">The method returns an instance of the dialog box.</span></span> <span data-ttu-id="6f8a1-123">Una vez establecidas las propiedades del cuadro de diálogo, se usa el método **IQuickFilingDialog.Run** para ejecutar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-123">Once the properties of the dialog box are set, the **IQuickFilingDialog.Run** method is used to run the dialog box.</span></span> <span data-ttu-id="6f8a1-124">Este método ejecuta el cuadro de diálogo en un subproceso nuevo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-124">This method runs the dialog box on a new thread.</span></span> 
  
<span data-ttu-id="6f8a1-125">**Properties**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-125">**Properties**</span></span>

|<span data-ttu-id="6f8a1-126">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-126">**Name**</span></span>|<span data-ttu-id="6f8a1-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-127">**Type**</span></span>|<span data-ttu-id="6f8a1-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6f8a1-129">**Title**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-129">**Title**</span></span> <br/> |<span data-ttu-id="6f8a1-130">string</span><span class="sxs-lookup"><span data-stu-id="6f8a1-130">string</span></span>  <br/> |<span data-ttu-id="6f8a1-131">Obtiene o establece el texto del título que aparece en la barra de título de la ventana del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-131">Gets or sets the title text that appears in the title bar of the dialog box window.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-132">**Description**</span></span> <br/> |<span data-ttu-id="6f8a1-133">string</span><span class="sxs-lookup"><span data-stu-id="6f8a1-133">string</span></span>  <br/> |<span data-ttu-id="6f8a1-134">Obtiene o establece la descripción del texto para indicar al usuario qué seleccionar.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-134">Gets or sets the text description to instruct the user about what to select.</span></span> <span data-ttu-id="6f8a1-135">Este valor puede ser texto de varias líneas.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-135">This value can be multiple-line text.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-136">**CheckboxText**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-136">**CheckboxText**</span></span> <br/> |<span data-ttu-id="6f8a1-137">string</span><span class="sxs-lookup"><span data-stu-id="6f8a1-137">string</span></span>  <br/> |<span data-ttu-id="6f8a1-138">Obtiene o establece el texto que sigue a la casilla.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-138">Gets or sets the text that follows the check box.</span></span> <span data-ttu-id="6f8a1-139">Si este valor se establece en una cadena no vacía, aparecerá una casilla en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-139">If this value is set to a non-empty string, a check box appears in the dialog box.</span></span> <span data-ttu-id="6f8a1-140">Si el valor es una cadena vacía, no aparece ninguna casilla.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-140">If the value is an empty string, no check box appears.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-141">**CheckboxState**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-141">**CheckboxState**</span></span> <br/> |<span data-ttu-id="6f8a1-142">bool</span><span class="sxs-lookup"><span data-stu-id="6f8a1-142">bool</span></span>  <br/> |<span data-ttu-id="6f8a1-143">Obtiene o establece el estado de la casilla.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-143">Gets or sets the state of the check box.</span></span> <span data-ttu-id="6f8a1-144">Si el valor se establece en **false,** la casilla se desactiva cuando se inicia el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-144">If value is set to **false**, the check box is cleared when the dialog box is started.</span></span> <span data-ttu-id="6f8a1-145">Si el valor se establece en **true,** la casilla de verificación se activa cuando se inicia el cuadro de diálogo siempre que **CheckboxText** sea una cadena no vacía.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-145">If the value is set to **true**, the check box is selected when the dialog box is started as long as **CheckboxText** is a non-empty string.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-146">**WindowHandle**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-146">**WindowHandle**</span></span> <br/> |<span data-ttu-id="6f8a1-147">ulong</span><span class="sxs-lookup"><span data-stu-id="6f8a1-147">ulong</span></span>  <br/> |<span data-ttu-id="6f8a1-148">Obtiene el identificador de la ventana del cuadro de diálogo Archivado rápido.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-148">Gets the handle ID of the Quick Filing dialog box window.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-149">**TreeDepth**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-149">**TreeDepth**</span></span> <br/> |<span data-ttu-id="6f8a1-150">**HierarchyElement**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-150">**HierarchyElement**</span></span> <br/> |<span data-ttu-id="6f8a1-151">Obtiene o establece la profundidad con la que se debe mostrar el árbol de OneNote en la sección Todos los blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-151">Gets or sets how deep the OneNote tree should be displayed in the All Notebooks section.</span></span> <span data-ttu-id="6f8a1-152">De forma predeterminada, el árbol se muestra hasta las secciones.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-152">By default, the tree is displayed up to the sections.</span></span> <span data-ttu-id="6f8a1-153">Esta propiedad no afecta al tipo de elementos que se pueden seleccionar.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-153">This property does not affect what type of elements can be selected.</span></span>  <br/> <span data-ttu-id="6f8a1-154">Si **TreeDepth** se establece en un elemento inferior en la jerarquía de OneNote de lo que puede seleccionar cualquiera de los botones, la profundidad de árbol mostrada será el elemento seleccionable más bajo posible.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-154">If **TreeDepth** is set to an element lower in the OneNote hierarchy than can be selected by any of the buttons, the displayed tree depth will be the lowest possible selectable element.</span></span> <span data-ttu-id="6f8a1-155">Es decir, si la profundidad del árbol está configurada para mostrarse en páginas, pero el elemento seleccionable más bajo es una sección, el árbol se muestra en secciones.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-155">That is, if tree depth is set to display down to pages, but the lowest selectable element is a section, the tree is displayed down to sections.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-156">**ParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-156">**ParentWindowHandle**</span></span> <br/> |<span data-ttu-id="6f8a1-157">ulong</span><span class="sxs-lookup"><span data-stu-id="6f8a1-157">ulong</span></span>  <br/> |<span data-ttu-id="6f8a1-158">Obtiene o establece el identificador de la ventana principal del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-158">Gets or sets the handle ID of the parent window of the dialog box.</span></span> <span data-ttu-id="6f8a1-159">Si se establece esta propiedad, el cuadro de diálogo Archivado rápido será modal para la ventana principal asignada cuando se abra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-159">If this property is set, the Quick Filing dialog box will be modal to the assigned parent window when the dialog box opens.</span></span> <span data-ttu-id="6f8a1-160">Es decir, un usuario no podrá tener acceso a la ventana principal hasta que se cierre el cuadro de diálogo Archivado rápido.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-160">That is, a user will not be able to access the parent window until the Quick Filing dialog box is closed.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-161">**Position**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-161">**Position**</span></span> <br/> |<span data-ttu-id="6f8a1-162">tagPOINT</span><span class="sxs-lookup"><span data-stu-id="6f8a1-162">tagPOINT</span></span>  <br/> |<span data-ttu-id="6f8a1-163">Obtiene o establece la posición de la ventana en relación con la pantalla.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-163">Gets or sets the position of the window in relation to the screen.</span></span> <span data-ttu-id="6f8a1-164">De forma predeterminada, el cuadro de diálogo aparece en medio de la ventana principal o del escritorio.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-164">By default, the dialog box appears in the middle of the parent window or the desktop.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-165">**SelectedItem**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-165">**SelectedItem**</span></span> <br/> |<span data-ttu-id="6f8a1-166">string</span><span class="sxs-lookup"><span data-stu-id="6f8a1-166">string</span></span>  <br/> |<span data-ttu-id="6f8a1-167">Obtiene el identificador de objeto de la ubicación de OneNote seleccionada por el usuario cuando se cierra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-167">Gets the object ID of the OneNote location selected by the user when the dialog box is closed.</span></span> <span data-ttu-id="6f8a1-168">Si el usuario hace clic en el **botón** Cancelar, el objeto se establece en null.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-168">If the user clicks the **Cancel** button, the object is set to null.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-169">**PressedButton**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-169">**PressedButton**</span></span> <br/> |<span data-ttu-id="6f8a1-170">ulong</span><span class="sxs-lookup"><span data-stu-id="6f8a1-170">ulong</span></span>  <br/> |<span data-ttu-id="6f8a1-171">Obtiene el botón en el que se hizo clic cuando se cerró el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-171">Gets which button was clicked when the dialog box was closed.</span></span> <span data-ttu-id="6f8a1-172">Si se **hizo** clic en el botón Cancelar, esta propiedad devuelve un valor de -1.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-172">If the **Cancel** button was clicked, this property returns a value of -1.</span></span> <span data-ttu-id="6f8a1-173">Todos los demás botones tienen asignados valores enteros de 0, incrementados en 1 por cada botón agregado al cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-173">All other buttons are assigned integer values from 0, incremented by 1 for each button added to the dialog box.</span></span> <span data-ttu-id="6f8a1-174">El valor entero del botón **Aceptar** predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-174">The integer value of the default **OK** button is 0.</span></span>  <br/> |
   
### <a name="methods"></a><span data-ttu-id="6f8a1-175">Methods</span><span class="sxs-lookup"><span data-stu-id="6f8a1-175">Methods</span></span>

<span data-ttu-id="6f8a1-176">**SetRecentResults**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-176">**SetRecentResults**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f8a1-177">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-177">**Description**</span></span> <br/> |<span data-ttu-id="6f8a1-178">Establece qué lista de resultados recientes se mostrará en el cuadro de diálogo Archivado rápido e indica si se deben incluir algunas ubicaciones de archivado especiales en la lista.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-178">Sets what recent result list will be displayed in the Quick Filing dialog box, and indicates whether to include some special filing locations in the list.</span></span> <span data-ttu-id="6f8a1-179">Los usuarios pueden seleccionar una lista de resultados recientes de la [enumeración RecentResultType.](enumerations-onenote-developer-reference.md#odc_RecentResultType)</span><span class="sxs-lookup"><span data-stu-id="6f8a1-179">Users can select a recent result list from the [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) enumeration.</span></span> <span data-ttu-id="6f8a1-180">Los usuarios también pueden elegir agregar las siguientes opciones a la lista: Sección actual, Página actual o Notas sin archivo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-180">Users can also choose to add the following options to the list: Current Section, Current Page, or Unfiled Notes.</span></span> <span data-ttu-id="6f8a1-181">Si **recentResultType.rrtNone** está seleccionado, no se muestra ninguna lista de resultados recientes.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-181">If **RecentResultType.rrtNone** is selected, no recent result list is shown.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-182">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-182">**Syntax**</span></span> <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|<span data-ttu-id="6f8a1-183">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-183">**Parameters**</span></span> <br/> | <span data-ttu-id="6f8a1-184">_recentResults_ &ndash; Objeto de tipo **RecentResultType** que indica qué lista de resultados recientes, si la hay, debe aparecer.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-184">_recentResults_ &ndash; An object of type **RecentResultType** that indicates which recent result list, if any, should appear.</span></span> <span data-ttu-id="6f8a1-185">Si **se selecciona rrtNone,** no aparece ninguna lista de resultados reciente en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-185">If **rrtNone** is selected, no recent result list appears in the dialog box.</span></span><br/><br/>  <span data-ttu-id="6f8a1-186">_fShowCurrentSection_ &ndash; Valor booleano que indica si la sección actual debe incluirse en la lista de resultados recientes.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-186">_fShowCurrentSection_ &ndash; A Boolean value that indicates whether the current section should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="6f8a1-187">_fShowCurrentPage_ &ndash; Un valor booleano que indica si la página actual debe incluirse en la lista de resultados recientes.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-187">_fShowCurrentPage_ &ndash; A Boolean value that indicates whether the current page should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="6f8a1-188">_fShowUnfiledNotes_ &ndash; Un valor booleano que indica si la sección Notas sin archivo debe incluirse en la lista de resultados recientes.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-188">_fShowUnfiledNotes_ &ndash; A Boolean value that indicates whether the Unfiled Notes section should be included in the recent result list.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="6f8a1-189">Si no se puede seleccionar una ubicación de archivado especial mediante cualquiera de los botones del cuadro de diálogo, no se muestra en la lista.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-189">If a special filing location cannot be selected by using any of the buttons in the dialog box, it is not shown in the list.</span></span> <span data-ttu-id="6f8a1-190">Si no se encuentra ningún elemento seleccionable en la lista de resultados recientes, no se muestra ninguna lista de resultados recientes.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-190">If no selectable item in the recent results list is found, no recent result list is displayed.</span></span> 
  
<span data-ttu-id="6f8a1-191">En el siguiente ejemplo se usa el **método SetRecentResults** para mostrar la sección actual, la página actual y la sección Notas sin archivo en la lista de resultados recientes.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-191">The following example uses the **SetRecentResults** method to display the current section, current page, and the Unfiled Notes section in the recent result list.</span></span> 
  
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

<span data-ttu-id="6f8a1-192">**AddButton**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-192">**AddButton**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f8a1-193">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-193">**Description**</span></span> <br/> |<span data-ttu-id="6f8a1-194">Permite a los usuarios agregar y personalizar botones en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-194">Allows users to add and customize buttons in the dialog box.</span></span> <span data-ttu-id="6f8a1-195">Los usuarios pueden especificar el texto de los botones y los elementos de la jerarquía de OneNote que puede seleccionar cada botón.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-195">Users can specify the text on the buttons and what elements of the OneNote hierarchy can be selected by each button.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-196">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-196">**Syntax**</span></span> <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|<span data-ttu-id="6f8a1-197">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-197">**Parameters**</span></span> <br/> | <span data-ttu-id="6f8a1-198">_bstrText_ &ndash; Cadena que especifica el texto que se mostrará en el botón.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-198">_bstrText_ &ndash; A string that specifies the text to appear on the button.</span></span> <span data-ttu-id="6f8a1-199">Para personalizar el botón **Aceptar** predeterminado, pase un valor nulo como **bstrText**.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-199">To customize the default **OK** button, pass in a null value as **bstrText**.</span></span>  <br/><br/><span data-ttu-id="6f8a1-200">_allowedElements_ &ndash; Elemento **HierarchyElement** que indica qué elementos de jerarquía de OneNote que no son de solo lectura que un usuario puede seleccionar con el botón.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-200">_allowedElements_ &ndash; A **HierarchyElement** that indicates what non-read-only OneNote hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="6f8a1-201">Para seleccionar varios elementos, el usuario debe pasar el operador **OR** para todos los valores equivalentes uint de los tipos **HierarchyElement** permitidos como **HierarchyElement**.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-201">For selecting multiple items, the user should pass in the **OR** operator for all the uint equivalent values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="6f8a1-202">_allowedReadOnlyElements_ &ndash; Elemento **HierarchyElement** que indica qué elementos de jerarquía de solo lectura de OneNote puede seleccionar un usuario mediante el botón.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-202">_allowedReadOnlyElements_ &ndash; A **HierarchyElement** that indicates what OneNote read-only hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="6f8a1-203">Para seleccionar varios elementos, el usuario debe pasar el operador **OR** para todos los valores **equivalentes uint** de los tipos **HierarchyElement** permitidos como **HierarchyElement**.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-203">For selecting multiple items, the user should pass in the **OR** operator for all the **uint** equivalents values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="6f8a1-204">_fDefault_ &ndash; Valor booleano que especifica si este botón debe ser el botón predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-204">_fDefault_ &ndash; A Boolean value that specifies whether this button should be the default button.</span></span> <span data-ttu-id="6f8a1-205">Si se establecen varios botones como predeterminados, el último botón especificado se convierte en el botón predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-205">If multiple buttons are set as default, the last specified button becomes the default button.</span></span>  <br/> |
   
<span data-ttu-id="6f8a1-206">En el siguiente ejemplo se agregan tres botones al cuadro de diálogo Archivado rápido.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-206">The following example adds three buttons to the Quick Filing dialog box.</span></span> <span data-ttu-id="6f8a1-207">Todos los elementos del árbol jerárquicos de OneNote pueden seleccionar el primero, Todos.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-207">The first one, **All**, can be selected by all elements in the OneNote hierarchy tree.</span></span> <span data-ttu-id="6f8a1-208">Los demás, **Blocs de notas** **y** páginas, solo se pueden seleccionar si se seleccionan sus elementos correspondientes, Blocs de notas y páginas.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-208">The others, **Notebooks** and **Pages**, can be selected only if their corresponding elements, Notebooks and Pages, are selected.</span></span>
  
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

<span data-ttu-id="6f8a1-209">**Run**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-209">**Run**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f8a1-210">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-210">**Description**</span></span> <br/> |<span data-ttu-id="6f8a1-211">Muestra el cuadro de diálogo Archivado rápido de un nuevo subproceso.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-211">Displays the Quick Filing dialog box from a new thread.</span></span> <span data-ttu-id="6f8a1-212">Toma una referencia a la interfaz **IQuickFilingDialogCallback,** cuyo **método OnDialogClosed** se llamará una vez que se cierre el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-212">It takes a reference to the **IQuickFilingDialogCallback** interface, whose **OnDialogClosed** method will be called once the dialog box closes.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-213">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-213">**Syntax**</span></span> <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|<span data-ttu-id="6f8a1-214">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-214">**Parameters**</span></span> <br/> | <span data-ttu-id="6f8a1-215">_piCallback_ &ndash; Una referencia a la **interfaz IQuickFilingDialogCallback** a la que se crearán instancias una vez que se cierre el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-215">_piCallback_ &ndash; A reference to the **IQuickFilingDialogCallback** interface that will be instantiated once the dialog box closes.</span></span>  <br/> |
   
<span data-ttu-id="6f8a1-216">En el siguiente ejemplo se usa **el método Run** para mostrar el cuadro de diálogo De archivado rápido de un nuevo subproceso.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-216">The following example uses the **Run** method to display the Quick Filing dialog box from a new thread.</span></span> 
  
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

<span data-ttu-id="6f8a1-217">**TreeCollapsedState**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-217">**TreeCollapsedState**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f8a1-218">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-218">**Description**</span></span> <br/> |<span data-ttu-id="6f8a1-219">Indica si el árbol de jerarquía debe expandirse o contraerse.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-219">Indicates whether the hierarchy tree should be expanded or collapsed.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-220">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-220">**Syntax**</span></span> <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|<span data-ttu-id="6f8a1-221">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-221">**Parameters**</span></span> <br/> | <span data-ttu-id="6f8a1-222">_tcs:_ especifica si el árbol está expandido o contraído.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-222">_tcs_ - Specifies whether the tree is expanded or collapsed.</span></span>  <br/> |
   
<span data-ttu-id="6f8a1-223">**NotebookFilterOut**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-223">**NotebookFilterOut**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f8a1-224">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-224">**Description**</span></span> <br/> |<span data-ttu-id="6f8a1-225">Filtra la lista de blocs de notas que se muestran por tipo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-225">Filters the list of notebooks shown by type.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-226">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-226">**Syntax**</span></span> <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|<span data-ttu-id="6f8a1-227">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-227">**Parameters**</span></span> <br/> | <span data-ttu-id="6f8a1-228">_nfo:_ especifica el conjunto de blocs de notas que se van a filtrar fuera de la lista.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-228">_nfo_ - Specifies the set of notebooks that are to be filtered out of the list</span></span>  <br/> |
   
<span data-ttu-id="6f8a1-229">**ShowCreateNewNotebook**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-229">**ShowCreateNewNotebook**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f8a1-230">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-230">**Description**</span></span> <br/> |<span data-ttu-id="6f8a1-231">Muestra la opción crear nuevo bloc de notas en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-231">Displays the create new notebook option in the dialog.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-232">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-232">**Syntax**</span></span> <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|<span data-ttu-id="6f8a1-233">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-233">**Parameters**</span></span> <br/> |<span data-ttu-id="6f8a1-234">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6f8a1-234">None</span></span>  <br/> |
   
<span data-ttu-id="6f8a1-235">**AddInitialEditor**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-235">**AddInitialEditor**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f8a1-236">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-236">**Description**</span></span> <br/> |<span data-ttu-id="6f8a1-237">Agrega un usuario como editor inicial a un bloc de notas en el cuadro de diálogo Archivado rápido.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-237">Adds a user as an initial editor to a notebook in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-238">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-238">**Syntax**</span></span> <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|<span data-ttu-id="6f8a1-239">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-239">**Parameters**</span></span> <br/> | <span data-ttu-id="6f8a1-240">_initialEditor:_ la dirección de correo electrónico del usuario que desea agregar como editor al bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-240">_initialEditor_ - The email address of the user you wish to add as an editor to the notebook.</span></span> <span data-ttu-id="6f8a1-241">Cuando el bloc de notas se crea mediante el cuadro de diálogo Archivado rápido, se comparte automáticamente con todos los editores iniciales.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-241">When the notebook is created via the Quick Filing dialog box, it is automatically shared with all Initial Editors.</span></span>  <br/> |
   
<span data-ttu-id="6f8a1-242">**ClearInitialEditors**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-242">**ClearInitialEditors**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f8a1-243">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-243">**Description**</span></span> <br/> |<span data-ttu-id="6f8a1-244">Quita todos los editores iniciales del cuadro de diálogo Archivado rápido.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-244">Removes all initial editors from the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-245">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-245">**Syntax**</span></span> <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|<span data-ttu-id="6f8a1-246">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-246">**Parameters**</span></span> <br/> |<span data-ttu-id="6f8a1-247">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6f8a1-247">None</span></span>  <br/> |
   
<span data-ttu-id="6f8a1-248">**ShowSharingHyperlink**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-248">**ShowSharingHyperlink**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f8a1-249">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-249">**Description**</span></span> <br/> |<span data-ttu-id="6f8a1-250">Muestra el hipervínculo del tema de ayuda para uso compartido en el cuadro de diálogo Archivado rápido.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-250">Displays the Sharing Help Topic Hyperlink in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-251">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-251">**Syntax**</span></span> <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|<span data-ttu-id="6f8a1-252">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-252">**Parameters**</span></span> <br/> |<span data-ttu-id="6f8a1-253">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6f8a1-253">None</span></span>  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a><span data-ttu-id="6f8a1-254">Interfaz IQuickFilingDialogCallback</span><span class="sxs-lookup"><span data-stu-id="6f8a1-254">IQuickFilingDialogCallback interface</span></span>
<span data-ttu-id="6f8a1-255"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="6f8a1-255"><a name="odc_IQuickFilingDialog"> </a></span></span>

<span data-ttu-id="6f8a1-256">Esta interfaz permite al usuario tener acceso a las propiedades del cuadro de diálogo después de cerrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-256">This interface allows the user to access the dialog box properties after the dialog box closes.</span></span> <span data-ttu-id="6f8a1-257">Una vez que se cierra el cuadro de diálogo, OneNote 2013 llama al método **IQuickFilingDialogCallback.OnDialogClose** en esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-257">Once the dialog box closes, OneNote 2013 calls the **IQuickFilingDialogCallback.OnDialogClose** method in this interface.</span></span> 
  
<span data-ttu-id="6f8a1-258">Debe definirse una clase que herede esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-258">A class that inherits this interface has to be defined.</span></span>
  
### <a name="methods"></a><span data-ttu-id="6f8a1-259">Methods</span><span class="sxs-lookup"><span data-stu-id="6f8a1-259">Methods</span></span>

<span data-ttu-id="6f8a1-260">En la siguiente sección se describen los métodos asociados con las interfaces detalladas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-260">The following section describes the methods associated with the interfaces detailed previously.</span></span>
  
<span data-ttu-id="6f8a1-261">**OnDialogClosed**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-261">**OnDialogClosed**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f8a1-262">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-262">**Description**</span></span> <br/> |<span data-ttu-id="6f8a1-263">Permite a los usuarios agregar funcionalidad para capturar y usar la selección de usuario desde el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-263">Enables users to add functionality to capture and use the user selection from the dialog box.</span></span> <span data-ttu-id="6f8a1-264">Se llama a este método después de cerrar el cuadro de diálogo Archivado rápido.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-264">This method is called after the Quick Filing dialog box is closed.</span></span> <span data-ttu-id="6f8a1-265">Este método es una función que las interfaces **IQuickFilingDialogCallback** tienen que definir.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-265">This method is a function that **IQuickFilingDialogCallback** interfaces have to define.</span></span>  <br/> |
|<span data-ttu-id="6f8a1-266">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-266">**Syntax**</span></span> <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|<span data-ttu-id="6f8a1-267">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-267">**Parameters**</span></span> <br/> | <span data-ttu-id="6f8a1-268">_dialog_ &ndash; Objeto **IQuickFilingDialog** que llamó al **método OnDialogClose.**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-268">_dialog_ &ndash; The **IQuickFilingDialog** object that called the **OnDialogClose** method.</span></span>  <br/> |
   
<span data-ttu-id="6f8a1-269">El siguiente ejemplo es una interfaz **de ejemplo IQuickFilingDialogCallback.**</span><span class="sxs-lookup"><span data-stu-id="6f8a1-269">The following example is a sample **IQuickFilingDialogCallback** interface.</span></span> <span data-ttu-id="6f8a1-270">El **método OnDialogClose** imprime la selección del usuario del cuadro de diálogo Archivado rápido en la consola.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-270">The **OnDialogClose** method prints the user's selection from the Quick Filing dialog box to the console.</span></span> 
  
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

## <a name="example"></a><span data-ttu-id="6f8a1-271">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f8a1-271">Example</span></span>
<span data-ttu-id="6f8a1-272"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="6f8a1-272"><a name="odc_IQuickFilingDialog"> </a></span></span>

<span data-ttu-id="6f8a1-273">En el siguiente ejemplo de código se abre un cuadro de diálogo de archivado rápido que tiene un título personalizado, una descripción, una lista de resultados recientes, una profundidad de árbol, una casilla de verificación y botones personalizados.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-273">The following code example opens a Quick Filing dialog box that has a customized title, description, recent result list, tree depth, check box, and buttons.</span></span> <span data-ttu-id="6f8a1-274">El elemento seleccionado del usuario, el botón presionado y el estado de la casilla de verificación se mostrarán en una ventana de consola cuando se cierre el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-274">The user's selected item, pressed button, and check-box state will be displayed in a console window when the dialog box is closed.</span></span> <span data-ttu-id="6f8a1-275">Para ver el botón de página habilitado, el usuario tendrá que buscar una página y seleccionarla, ya que la profundidad del árbol se establece en secciones.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-275">To see the page button enabled, the user will have to search for a page and select it, because the tree depth is set down to sections.</span></span> <span data-ttu-id="6f8a1-276">El cuadro de diálogo no es un elemento secundario de ninguna ventana.</span><span class="sxs-lookup"><span data-stu-id="6f8a1-276">The dialog box is not a child of any window.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="6f8a1-277">Ver también</span><span class="sxs-lookup"><span data-stu-id="6f8a1-277">See also</span></span>

- [<span data-ttu-id="6f8a1-278">Referencia para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="6f8a1-278">OneNote developer reference</span></span>](onenote-developer-reference.md)

