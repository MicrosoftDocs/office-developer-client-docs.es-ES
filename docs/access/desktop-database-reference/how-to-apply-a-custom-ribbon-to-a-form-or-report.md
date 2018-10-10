---
title: Aplicar una cinta de opciones personalizada a un formulario o informe
TOCTitle: Apply a custom ribbon to a form or report
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4fb0155b1a1ed36b6fe924f72a4da385197cc21
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485918"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a><span data-ttu-id="9e004-102">Aplicar una cinta de opciones personalizada a un formulario o informe</span><span class="sxs-lookup"><span data-stu-id="9e004-102">Apply a custom ribbon to a form or report</span></span>


<span data-ttu-id="9e004-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e004-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9e004-p101">La cinta usa marcado XML declarativo basado en texto que simplifica su creación y personalización. Con unas pocas líneas de XML se puede crear la interfaz adecuada para el usuario. Access proporciona flexibilidad a la hora de personalizar la interfaz de usuario de la cinta. Por ejemplo, el marcado de personalización se puede almacenar en una tabla, insertar en un procedimiento de VBA, almacenar en otra base de datos de Access o vincular desde una hoja de cálculo de Excel. En este tema se explica cómo aplicar cintas personalizadas al cargar un formulario o un informe.</span><span class="sxs-lookup"><span data-stu-id="9e004-p101">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon. With a few lines of XML, you can create just the right interface for the user. Access provides flexibility in customizing the ribbon user interface. For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet. This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="9e004-109">Activar la personalización de la cinta XML</span><span class="sxs-lookup"><span data-stu-id="9e004-109">Making the Ribbon Customization XML Available</span></span>

<span data-ttu-id="9e004-110">**Almacenar la extensibilidad de la cinta XML en una tabla**</span><span class="sxs-lookup"><span data-stu-id="9e004-110">**Storing Ribbon Extensibility XML in a Table**</span></span>

<span data-ttu-id="9e004-p102">Un método que puede usar para que las personalizaciones de la cinta estén disponibles es almacenarlas en una tabla. Si las almacena en una tabla denominada **USysRibbons**, las personalizaciones se pueden implementar sin usar macros o código VBA.</span><span class="sxs-lookup"><span data-stu-id="9e004-p102">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="9e004-p103">**USysRibbons** es una tabla del sistema creada por el usuario. La tabla se debe crear con nombres de columna específicos para que se implementen las personalizaciones de la cinta. La siguiente tabla muestra la configuración para usar al crear la tabla **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="9e004-p103">**USysRibbons** is a user-created system table. The table must be created using specific column names in order for the ribbon customizations to be implemented. The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e004-116">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="9e004-116">Column Name</span></span></p></th>
<th><p><span data-ttu-id="9e004-117">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9e004-117">Data Type</span></span></p></th>
<th><p><span data-ttu-id="9e004-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e004-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e004-119"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="9e004-119"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="9e004-120">Texto</span><span class="sxs-lookup"><span data-stu-id="9e004-120">Text</span></span></p></td>
<td><p><span data-ttu-id="9e004-121">Contiene el nombre de la cinta personalizada que se asociará a esta personalización.</span><span class="sxs-lookup"><span data-stu-id="9e004-121">Contains the name of the custom ribbon to be associated with this customization</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e004-122"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="9e004-122"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="9e004-123">Memo</span><span class="sxs-lookup"><span data-stu-id="9e004-123">Memo</span></span></p></td>
<td><p><span data-ttu-id="9e004-124">Contiene el XML de extensibilidad de cinta (RibbonX) que define la personalización de la cinta.</span><span class="sxs-lookup"><span data-stu-id="9e004-124">Contains the ribbon Extensibility XML (RibbonX) that defines the ribbon customization</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9e004-125">**Cargar XML de extensibilidad de cinta mediante programación**</span><span class="sxs-lookup"><span data-stu-id="9e004-125">**Loading Ribbon Extensibility XML Programmatically**</span></span>

<span data-ttu-id="9e004-p104">Puede usar el método **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** para cargar las personalizaciones de la cinta mediante programación. Normalmente, para crear y hacer que la cinta esté disponible para la aplicación, primero debe crear un módulo en la base de datos con un procedimiento que llame al método **LoadCustomUI**, pasando el nombre de la cinta y el marcado de personalización XML.</span><span class="sxs-lookup"><span data-stu-id="9e004-p104">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="9e004-p105">El marcado de personalización XML puede venir de un objeto **Recordset** creado desde una tabla, desde un origen externo a la base de datos como un archivo XML que debe analizar en una cadena, o desde un marcado XML insertado directamente en el procedimiento. Puede crear varias cintas con varias llamadas al método **LoadCustomUI**, pasando un marcado XML diferente siempre que el nombre de cada cinta y el atributo **id** de las pestañas que conforman la cinta sean únicas.</span><span class="sxs-lookup"><span data-stu-id="9e004-p105">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="9e004-p106">Una vez completado el procedimiento, cree una macro AutoExec que llame al procedimiento con la acción RunCode. De este modo, cuando se inicia la aplicación, el método **LoadCustomUI** se ejecuta automáticamente y todas las cintas personalizadas estarán disponibles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9e004-p106">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action. That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="assigning-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="9e004-132">Asignar cintas personalizadas a formularios o informes</span><span class="sxs-lookup"><span data-stu-id="9e004-132">Assigning Custom Ribbons to Forms or Reports</span></span>

1.  <span data-ttu-id="9e004-133">Siga el proceso descrito previamente para poner la Cinta de opciones personalizada a disposición de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9e004-133">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="9e004-134">Abra el formulario o informe en la vista Diseño.</span><span class="sxs-lookup"><span data-stu-id="9e004-134">Open the form or report in Design view.</span></span>

3.  <span data-ttu-id="9e004-135">En la pestaña Diseño, haga clic en **Hoja de propiedades**.</span><span class="sxs-lookup"><span data-stu-id="9e004-135">On the Design tab, click **Property Sheet**.</span></span>

4.  <span data-ttu-id="9e004-136">En la ficha **Todos** de la ventana Propiedad, haga clic en la lista **Nombre de banda de opciones** y, a continuación, seleccione una cinta.</span><span class="sxs-lookup"><span data-stu-id="9e004-136">On the **All** tab of the Property window, click the **Ribbon Name** list and then select a ribbon.</span></span>

5.  <span data-ttu-id="9e004-p107">Guarde, cierre y vuelva a abrir el formulario o el informe. Se muestra la IU de la cinta que ha seleccionado.</span><span class="sxs-lookup"><span data-stu-id="9e004-p107">Save, close, and then reopen the form or report. The ribbon UI you selected is displayed.</span></span>


> [!NOTE]
> <span data-ttu-id="9e004-139">Las fichas mostradas en la interfaz de usuario de la cinta de opciones son aditivos.</span><span class="sxs-lookup"><span data-stu-id="9e004-139">The tabs displayed in the ribbon UI are additive.</span></span> <span data-ttu-id="9e004-140">Es decir, a menos que oculte las fichas específicamente o establezca el atributo *empezar desde el principio* en **True**, las fichas que se muestran en un formulario o interfaz de usuario de la cinta de opciones del informe son además de las fichas existentes.</span><span class="sxs-lookup"><span data-stu-id="9e004-140">That is, unless you specifically hide the tabs or set the *Start from Scratch* attribute to **True**, the tabs displayed in a form's or report's ribbon user interface are in addition to the existing tabs.</span></span>

> [!NOTE]
> <span data-ttu-id="9e004-141">[!NOTA] Para obtener más información sobre la interfaz de usuario de la cinta en otras aplicaciones de Office, consulte [Información general de la cinta de Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="9e004-141">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


