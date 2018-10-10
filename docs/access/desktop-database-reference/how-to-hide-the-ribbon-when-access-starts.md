---
title: Ocultar la cinta de opciones al iniciar Access
TOCTitle: Hide the ribbon when Access starts
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b2b3e28157662a585fa03353da92a598b96bd2c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483998"
---
# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="b15eb-102">Ocultar la cinta de opciones al iniciar Access</span><span class="sxs-lookup"><span data-stu-id="b15eb-102">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="b15eb-103">**Se aplica a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b15eb-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="b15eb-p101">De manera predeterminada, Microsoft Access no dispone de un método para ocultar la cinta. En este tema se describe de qué manera se puede cargar una cinta personalizada que oculte todas las fichas integradas.</span><span class="sxs-lookup"><span data-stu-id="b15eb-p101">By default, Microsoft Access does not provide a method for hiding the ribbon. This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="b15eb-106">Para cargar la Cinta de opciones personalizada al iniciar Access, deberá almacenar su configuración en una tabla denominada **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="b15eb-106">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="b15eb-p102">La tabla **USysRibbons** deberá crearse utilizando nombres de columna específicos para que las personalizaciones de la Cinta de opciones se puedan implementar. La tabla siguiente describe la configuración que se utilizará al crear la tabla **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="b15eb-p102">The **USysRibbons** table must be created using specific column names in order for the ribbon customizations to be implemented. The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b15eb-109">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="b15eb-109">Column Name</span></span></p></th>
<th><p><span data-ttu-id="b15eb-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b15eb-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b15eb-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b15eb-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b15eb-112"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="b15eb-112"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="b15eb-113">Texto</span><span class="sxs-lookup"><span data-stu-id="b15eb-113">Text</span></span></p></td>
<td><p><span data-ttu-id="b15eb-114">Contiene el nombre de la Cinta de opciones personalizada que se asociará a esta personalización.</span><span class="sxs-lookup"><span data-stu-id="b15eb-114">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b15eb-115"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="b15eb-115"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="b15eb-116">Memo</span><span class="sxs-lookup"><span data-stu-id="b15eb-116">Memo</span></span></p></td>
<td><p><span data-ttu-id="b15eb-117">Contiene el código XML de extensibilidad de la Cinta de opciones (RibbonX) que define la personalización de la Cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="b15eb-117">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b15eb-118">La tabla siguiente describe los valores de personalización de la Cinta de opciones que se deben almacenar en la tabla **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="b15eb-118">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b15eb-119">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="b15eb-119">Column Name</span></span></p></th>
<th><p><span data-ttu-id="b15eb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b15eb-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b15eb-121"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="b15eb-121"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="b15eb-122">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="b15eb-122">HideTheRibbon</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b15eb-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="b15eb-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="b15eb-124">&lt;CustomUI xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot; &gt; &lt;la cinta de opciones startFromScratch =&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span><span class="sxs-lookup"><span data-stu-id="b15eb-124">&lt;CustomUI xmlns=&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot;&gt; &lt;ribbon startFromScratch=&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="b15eb-125">Aplicar la Cinta de opciones personalizada al iniciar Access</span><span class="sxs-lookup"><span data-stu-id="b15eb-125">Applying a Custom Ribbon When Access Starts</span></span>

<span data-ttu-id="b15eb-126">Para implementar una interfaz de usuario personalizada con objeto de que esté disponible al iniciarse la aplicación, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b15eb-126">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="b15eb-127">Siga el proceso descrito previamente para poner la Cinta de opciones personalizada a disposición de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b15eb-127">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="b15eb-128">Cierre la aplicación y, a continuación, reiníciela.</span><span class="sxs-lookup"><span data-stu-id="b15eb-128">Close and then restart the application.</span></span>

3.  <span data-ttu-id="b15eb-129">Haga clic en el **Botón de Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") y, a continuación, haga clic en **Opciones de Access**.</span><span class="sxs-lookup"><span data-stu-id="b15eb-129">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="b15eb-130">Haga clic en la opción **Base de datos activa** y, a continuación, en la sección **Opciones de barra de herramientas y de la cinta de opciones**, haga clic en la lista **Nombre de cinta de opciones** y seleccione **HideTheRibbon**.</span><span class="sxs-lookup"><span data-stu-id="b15eb-130">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select **HideTheRibbon**.</span></span>

5.  <span data-ttu-id="b15eb-131">Cierre y vuelva a iniciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b15eb-131">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="b15eb-132">[!NOTA] Para obtener más información sobre la interfaz de usuario de la cinta en otras aplicaciones de Office, consulte [Información general de la cinta de Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="b15eb-132">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


