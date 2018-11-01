---
title: Aplicar una cinta de opciones personalizada a un formulario o un informe
TOCTitle: Apply a custom ribbon to a form or report
description: Cómo aplicar cintas de opciones personalizadas al cargar un formulario o informe en Access 2013.
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 10/16/2018
mtps_version: v=office.15
ms.openlocfilehash: e494985054ffd91440f3aff6eb671b781a5f65d7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888828"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a><span data-ttu-id="0929d-103">Aplicar una cinta de opciones personalizada a un formulario o un informe</span><span class="sxs-lookup"><span data-stu-id="0929d-103">Apply a custom ribbon to a form or report</span></span>

<span data-ttu-id="0929d-104">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0929d-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0929d-105">La cinta usa el marcado XML declarativa basada en texto que simplifica la creación y personalización de la cinta.</span><span class="sxs-lookup"><span data-stu-id="0929d-105">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="0929d-106">Con unas pocas líneas de XML se puede crear la interfaz adecuada para el usuario.</span><span class="sxs-lookup"><span data-stu-id="0929d-106">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="0929d-107">Access proporciona flexibilidad a la hora de personalizar la interfaz de usuario de la cinta.</span><span class="sxs-lookup"><span data-stu-id="0929d-107">Access provides flexibility in customizing the ribbon user interface.</span></span> 

<span data-ttu-id="0929d-108">Por ejemplo, el marcado de personalización se puede almacenar en una tabla, insertar en un procedimiento de VBA, almacenar en otra base de datos de Access o vincular desde una hoja de cálculo de Excel.</span><span class="sxs-lookup"><span data-stu-id="0929d-108">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="0929d-109">En este tema se explica cómo aplicar cintas personalizadas al cargar un formulario o un informe.</span><span class="sxs-lookup"><span data-stu-id="0929d-109">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="0929d-110">Poner a disposición de la personalización de la cinta de opciones XML</span><span class="sxs-lookup"><span data-stu-id="0929d-110">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="0929d-111">Almacenar código XML de extensibilidad de la cinta de opciones en una tabla</span><span class="sxs-lookup"><span data-stu-id="0929d-111">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="0929d-p103">Un método que puede usar para que las personalizaciones de la cinta estén disponibles es almacenarlas en una tabla. Si las almacena en una tabla denominada **USysRibbons**, las personalizaciones se pueden implementar sin usar macros o código VBA.</span><span class="sxs-lookup"><span data-stu-id="0929d-p103">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="0929d-114">**USysRibbons** es una tabla del sistema creada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="0929d-114">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="0929d-115">La tabla debe crearse utilizando nombres de columna específicos para las personalizaciones de la cinta de opciones para se puedan implementar.</span><span class="sxs-lookup"><span data-stu-id="0929d-115">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="0929d-116">La tabla siguiente describe la configuración que se utilizará al crear la tabla **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="0929d-116">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0929d-117">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="0929d-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="0929d-118">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0929d-118">Data type</span></span></p></th>
<th><p><span data-ttu-id="0929d-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="0929d-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0929d-120"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="0929d-120"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="0929d-121">Texto</span><span class="sxs-lookup"><span data-stu-id="0929d-121">Text</span></span></p></td>
<td><p><span data-ttu-id="0929d-122">Contiene el nombre de la Cinta de opciones personalizada que se asociará a esta personalización.</span><span class="sxs-lookup"><span data-stu-id="0929d-122">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0929d-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="0929d-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="0929d-124">Memo</span><span class="sxs-lookup"><span data-stu-id="0929d-124">Memo</span></span></p></td>
<td><p><span data-ttu-id="0929d-125">Contiene el XML (RibbonX) que define la personalización de la cinta de opciones de extensibilidad de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="0929d-125">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="0929d-126">Cargar el código XML de extensibilidad de la cinta de opciones mediante programación</span><span class="sxs-lookup"><span data-stu-id="0929d-126">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="0929d-p105">Puede usar el método **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** para cargar las personalizaciones de la cinta mediante programación. Normalmente, para crear y hacer que la cinta esté disponible para la aplicación, primero debe crear un módulo en la base de datos con un procedimiento que llame al método **LoadCustomUI**, pasando el nombre de la cinta y el marcado de personalización XML.</span><span class="sxs-lookup"><span data-stu-id="0929d-p105">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="0929d-p106">El marcado de personalización XML puede venir de un objeto **Recordset** creado desde una tabla, desde un origen externo a la base de datos como un archivo XML que debe analizar en una cadena, o desde un marcado XML insertado directamente en el procedimiento. Puede crear varias cintas con varias llamadas al método **LoadCustomUI**, pasando un marcado XML diferente siempre que el nombre de cada cinta y el atributo **id** de las pestañas que conforman la cinta sean únicas.</span><span class="sxs-lookup"><span data-stu-id="0929d-p106">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="0929d-p107">Una vez completado el procedimiento, cree una macro AutoExec que llame al procedimiento con la acción RunCode. De este modo, cuando se inicia la aplicación, el método **LoadCustomUI** se ejecuta automáticamente y todas las cintas personalizadas estarán disponibles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0929d-p107">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action. That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="assign-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="0929d-133">Asignar cintas de opciones personalizadas a formularios o informes</span><span class="sxs-lookup"><span data-stu-id="0929d-133">Assign custom ribbons to forms or reports</span></span>

1.  <span data-ttu-id="0929d-134">Siga el proceso descrito previamente para poner la Cinta de opciones personalizada a disposición de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0929d-134">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="0929d-135">Abra el formulario o informe en la vista Diseño.</span><span class="sxs-lookup"><span data-stu-id="0929d-135">Open the form or report in Design view.</span></span>

3.  <span data-ttu-id="0929d-136">En la ficha Diseño, elija **Hoja de propiedades**.</span><span class="sxs-lookup"><span data-stu-id="0929d-136">On the Design tab, choose **Property Sheet**.</span></span>

4.  <span data-ttu-id="0929d-137">En la ficha **todos** de la ventana Propiedades, elija la lista **Nombre de la cinta de opciones** y, a continuación, seleccione una cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="0929d-137">On the **All** tab of the Property window, choose the **Ribbon Name** list and then select a ribbon.</span></span>

5.  <span data-ttu-id="0929d-p108">Guarde, cierre y vuelva a abrir el formulario o el informe. Se muestra la IU de la cinta que ha seleccionado.</span><span class="sxs-lookup"><span data-stu-id="0929d-p108">Save, close, and then reopen the form or report. The ribbon UI you selected is displayed.</span></span>


> [!NOTE]
> <span data-ttu-id="0929d-140">Las fichas mostradas en la interfaz de usuario de la cinta de opciones son aditivos.</span><span class="sxs-lookup"><span data-stu-id="0929d-140">The tabs displayed in the ribbon UI are additive.</span></span> <span data-ttu-id="0929d-141">Es decir, a menos que oculte las fichas específicamente o establezca el atributo *empezar desde el principio* en **True**, las fichas que se muestran en un formulario o interfaz de usuario de la cinta de opciones del informe son además de las fichas existentes.</span><span class="sxs-lookup"><span data-stu-id="0929d-141">That is, unless you specifically hide the tabs or set the *Start from Scratch* attribute to **True**, the tabs displayed in a form's or report's ribbon user interface are in addition to the existing tabs.</span></span>

> [!NOTE]
> <span data-ttu-id="0929d-142">[!NOTA] Para obtener más información sobre la interfaz de usuario de la cinta en otras aplicaciones de Office, consulte [Información general de la cinta de Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="0929d-142">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


