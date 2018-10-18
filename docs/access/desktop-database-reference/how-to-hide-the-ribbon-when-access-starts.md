---
<span data-ttu-id="f9695-101">título: ocultar la cinta de opciones al iniciar Access TOCTitle: ocultar la cinta de opciones al iniciar Access <<<<<<< HEAD ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: ms.date 48548817: 18/09/2015 === Descripción: cómo cargar una cinta de opciones personalizada que oculte todas las fichas integradas en Access 2013.</span><span class="sxs-lookup"><span data-stu-id="f9695-101">title: Hide the ribbon when Access starts TOCTitle: Hide the ribbon when Access starts <<<<<<< HEAD ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 09/18/2015 ======= description: How to load a customized ribbon that hides all of the built-in tabs in Access 2013.</span></span>
<span data-ttu-id="f9695-102">MS:AssetId: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: ms.date 48548817: 16/10/2018</span><span class="sxs-lookup"><span data-stu-id="f9695-102">ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="f9695-103">mtps_version principal: Office.15</span><span class="sxs-lookup"><span data-stu-id="f9695-103">master mtps_version: v=office.15</span></span>
---

# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="f9695-104">Ocultar la cinta de opciones al iniciar Access</span><span class="sxs-lookup"><span data-stu-id="f9695-104">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="f9695-105">**Se aplica a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9695-105">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="f9695-p102">De manera predeterminada, Microsoft Access no dispone de un método para ocultar la cinta. En este tema se describe de qué manera se puede cargar una cinta personalizada que oculte todas las fichas integradas.</span><span class="sxs-lookup"><span data-stu-id="f9695-p102">By default, Microsoft Access does not provide a method for hiding the ribbon. This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="f9695-108">Para cargar la Cinta de opciones personalizada al iniciar Access, deberá almacenar su configuración en una tabla denominada **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="f9695-108">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="f9695-109"><<<<<<< Encabezado de la tabla **USysRibbons** debe crearse utilizando nombres de columna específicos en orden para las personalizaciones de la cinta de opciones para se puedan implementar.</span><span class="sxs-lookup"><span data-stu-id="f9695-109"><<<<<<< HEAD The **USysRibbons** table must be created using specific column names in order for the ribbon customizations to be implemented.</span></span> <span data-ttu-id="f9695-110">La tabla siguiente describe la configuración que se utilizará al crear la tabla **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="f9695-110">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
<span data-ttu-id="f9695-111">=== La tabla **USysRibbons** debe crearse utilizando nombres de columna específicos para las personalizaciones de la cinta de opciones para se puedan implementar.</span><span class="sxs-lookup"><span data-stu-id="f9695-111">======= The **USysRibbons** table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="f9695-112">La tabla siguiente describe la configuración que se utilizará al crear la tabla **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="f9695-112">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
>>>>>>> <span data-ttu-id="f9695-113">master</span><span class="sxs-lookup"><span data-stu-id="f9695-113">master</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<span data-ttu-id="f9695-114"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f9695-114"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="f9695-115">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="f9695-115">Column Name</span></span></p></th>
<th><p><span data-ttu-id="f9695-116">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f9695-116">Data Type</span></span></p></th>
=======
<th><p><span data-ttu-id="f9695-117">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="f9695-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="f9695-118">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f9695-118">Data type</span></span></p></th><span data-ttu-id="f9695-119">
>>>>>>>patrón</span><span class="sxs-lookup"><span data-stu-id="f9695-119">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="f9695-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9695-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9695-121"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="f9695-121"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="f9695-122">Texto</span><span class="sxs-lookup"><span data-stu-id="f9695-122">Text</span></span></p></td>
<td><p><span data-ttu-id="f9695-123">Contiene el nombre de la Cinta de opciones personalizada que se asociará a esta personalización.</span><span class="sxs-lookup"><span data-stu-id="f9695-123">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9695-124"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="f9695-124"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="f9695-125">Memo</span><span class="sxs-lookup"><span data-stu-id="f9695-125">Memo</span></span></p></td>
<span data-ttu-id="f9695-126"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f9695-126"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="f9695-127">Contiene el código XML de extensibilidad de la Cinta de opciones (RibbonX) que define la personalización de la Cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="f9695-127">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
=======
<td><p><span data-ttu-id="f9695-128">Contiene el XML (RibbonX) que define la personalización de la cinta de opciones de extensibilidad de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="f9695-128">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td><span data-ttu-id="f9695-129">
>>>>>>>patrón</span><span class="sxs-lookup"><span data-stu-id="f9695-129">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>

<span data-ttu-id="f9695-130"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f9695-130"><<<<<<< HEAD</span></span>

<span data-ttu-id="f9695-131">La tabla siguiente describe los valores de personalización de la Cinta de opciones que se deben almacenar en la tabla **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="f9695-131">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9695-132">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="f9695-132">Column Name</span></span></p></th>
<th><p><span data-ttu-id="f9695-133">Valor</span><span class="sxs-lookup"><span data-stu-id="f9695-133">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9695-134"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="f9695-134"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="f9695-135">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="f9695-135">HideTheRibbon</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9695-136"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="f9695-136"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="f9695-137">&lt;CustomUI xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot; &gt; &lt;la cinta de opciones startFromScratch =&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span><span class="sxs-lookup"><span data-stu-id="f9695-137">&lt;CustomUI xmlns=&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot;&gt; &lt;ribbon startFromScratch=&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="f9695-138">Aplicar la Cinta de opciones personalizada al iniciar Access</span><span class="sxs-lookup"><span data-stu-id="f9695-138">Applying a Custom Ribbon When Access Starts</span></span>
=======
<br/>

<span data-ttu-id="f9695-139">La tabla siguiente describe los valores de personalización de la Cinta de opciones que se deben almacenar en la tabla **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="f9695-139">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

|<span data-ttu-id="f9695-140">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="f9695-140">Column name</span></span>|<span data-ttu-id="f9695-141">Valor</span><span class="sxs-lookup"><span data-stu-id="f9695-141">Value</span></span>|
|:----------|:----|
|<span data-ttu-id="f9695-142">**RibbonName**</span><span class="sxs-lookup"><span data-stu-id="f9695-142">**RibbonName**</span></span>|<span data-ttu-id="f9695-143">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="f9695-143">HideTheRibbon</span></span>|
|<span data-ttu-id="f9695-144">**RibbonXML**</span><span class="sxs-lookup"><span data-stu-id="f9695-144">**RibbonXML**</span></span>|`<CustomUI xmlns="https://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="f9695-145">Aplicar una cinta de opciones personalizada al iniciar Access</span><span class="sxs-lookup"><span data-stu-id="f9695-145">Apply a custom ribbon when Access starts</span></span>
>>>>>>> <span data-ttu-id="f9695-146">master</span><span class="sxs-lookup"><span data-stu-id="f9695-146">master</span></span>

<span data-ttu-id="f9695-147">Para implementar una interfaz de usuario personalizada con objeto de que esté disponible al iniciarse la aplicación, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f9695-147">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="f9695-148">Siga el proceso descrito previamente para poner la Cinta de opciones personalizada a disposición de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f9695-148">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="f9695-149">Cierre la aplicación y, a continuación, reiníciela.</span><span class="sxs-lookup"><span data-stu-id="f9695-149">Close and then restart the application.</span></span>

<span data-ttu-id="f9695-150"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="f9695-150"><<<<<<< HEAD</span></span>
3.  <span data-ttu-id="f9695-151">Haga clic en el **Botón de Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") y, a continuación, haga clic en **Opciones de Access**.</span><span class="sxs-lookup"><span data-stu-id="f9695-151">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="f9695-152">Haga clic en la opción **Base de datos activa** y, a continuación, en la sección **Opciones de barra de herramientas y de la cinta de opciones**, haga clic en la lista **Nombre de cinta de opciones** y seleccione **HideTheRibbon**.</span><span class="sxs-lookup"><span data-stu-id="f9695-152">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select **HideTheRibbon**.</span></span>
=======
3.  <span data-ttu-id="f9695-153">Elija el **Botón de Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102")y, a continuación, elija **Opciones de Access**.</span><span class="sxs-lookup"><span data-stu-id="f9695-153">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="f9695-154">Elija la opción de **Base de datos actual** y, a continuación, en la sección **Opciones de barra de herramientas y la cinta de opciones** , elija la lista **Nombre de la cinta de opciones** y seleccione **HideTheRibbon**.</span><span class="sxs-lookup"><span data-stu-id="f9695-154">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select **HideTheRibbon**.</span></span>
>>>>>>> <span data-ttu-id="f9695-155">master</span><span class="sxs-lookup"><span data-stu-id="f9695-155">master</span></span>

5.  <span data-ttu-id="f9695-156">Cierre y vuelva a iniciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f9695-156">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="f9695-157">[!NOTA] Para obtener más información sobre la interfaz de usuario de la cinta en otras aplicaciones de Office, consulte [Información general de la cinta de Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="f9695-157">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


