---
title: Ocultar la cinta de opciones al iniciar Access
TOCTitle: Hide the ribbon when Access starts
description: Cómo cargar una cinta personalizada que oculte todas las fichas integradas en Access 2013.
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 384a575ae5e15b75ba7b0b891529c695cc3de599
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537832"
---
# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="c754b-103">Ocultar la cinta de opciones al iniciar Access</span><span class="sxs-lookup"><span data-stu-id="c754b-103">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="c754b-104">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c754b-104">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="c754b-p101">De manera predeterminada, Microsoft Access no dispone de un método para ocultar la cinta. En este tema se describe de qué manera se puede cargar una cinta personalizada que oculte todas las fichas integradas.</span><span class="sxs-lookup"><span data-stu-id="c754b-p101">By default, Microsoft Access does not provide a method for hiding the ribbon. This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="c754b-107">Para cargar la Cinta de opciones personalizada al iniciar Access, deberá almacenar su configuración en una tabla denominada **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="c754b-107">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="c754b-108">La tabla **USysRibbons** deberá crearse utilizando nombres de columna específicos para que las personalizaciones de la Cinta de opciones se puedan implementar.</span><span class="sxs-lookup"><span data-stu-id="c754b-108">The **USysRibbons** table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="c754b-109">La tabla siguiente muestra la configuración para crear la tabla **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="c754b-109">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c754b-110">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="c754b-110">Column name</span></span></p></th>
<th><p><span data-ttu-id="c754b-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c754b-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="c754b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c754b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c754b-113"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="c754b-113"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="c754b-114">Text</span><span class="sxs-lookup"><span data-stu-id="c754b-114">Text</span></span></p></td>
<td><p><span data-ttu-id="c754b-115">Contiene el nombre de la Cinta de opciones personalizada que se asociará a esta personalización.</span><span class="sxs-lookup"><span data-stu-id="c754b-115">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c754b-116"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="c754b-116"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="c754b-117">Notas</span><span class="sxs-lookup"><span data-stu-id="c754b-117">Memo</span></span></p></td>
<td><p><span data-ttu-id="c754b-118">Contiene el código XML de extensibilidad de la cinta de opciones (RibbonX) que define la personalización de la Cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="c754b-118">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="c754b-119">La tabla siguiente muestra la configuración de personalización de la cinta de opciones para almacenar en la tabla **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="c754b-119">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

|<span data-ttu-id="c754b-120">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="c754b-120">Column name</span></span>|<span data-ttu-id="c754b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c754b-121">Value</span></span>|
|:----------|:----|
|<span data-ttu-id="c754b-122">**RibbonName**</span><span class="sxs-lookup"><span data-stu-id="c754b-122">**RibbonName**</span></span>|<span data-ttu-id="c754b-123">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="c754b-123">HideTheRibbon</span></span>|
|<span data-ttu-id="c754b-124">**RibbonXML**</span><span class="sxs-lookup"><span data-stu-id="c754b-124">**RibbonXML**</span></span>|`<CustomUI xmlns="http://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="c754b-125">Aplicar una cinta de opciones personalizada al iniciar Access</span><span class="sxs-lookup"><span data-stu-id="c754b-125">Apply a custom ribbon when Access starts</span></span>

<span data-ttu-id="c754b-126">Para implementar una interfaz de usuario personalizada con objeto de que esté disponible al iniciarse la aplicación, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c754b-126">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="c754b-127">Siga el proceso descrito previamente para poner la Cinta de opciones personalizada a disposición de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c754b-127">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="c754b-128">Cierre la aplicación y, a continuación, reiníciela.</span><span class="sxs-lookup"><span data-stu-id="c754b-128">Close and then restart the application.</span></span>

3.  <span data-ttu-id="c754b-129">Elija el **botón Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") y luego elija **Opciones de Access**.</span><span class="sxs-lookup"><span data-stu-id="c754b-129">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="c754b-130">Seleccione la opción **Base de datos activa** y, en la sección **Opciones de barra de herramientas y de la cinta de opciones**, haga clic en la lista **Nombre de cinta de opciones** y seleccione **HideTheRibbon**.</span><span class="sxs-lookup"><span data-stu-id="c754b-130">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select **HideTheRibbon**.</span></span>

5.  <span data-ttu-id="c754b-131">Cierre y vuelva a iniciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c754b-131">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="c754b-132">Para obtener más información sobre la interfaz de usuario de la cinta en otras aplicaciones de Office, consulte [Información general de la cinta de Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="c754b-132">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


