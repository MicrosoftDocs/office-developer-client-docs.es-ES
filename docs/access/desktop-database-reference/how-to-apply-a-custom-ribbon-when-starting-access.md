---
title: Aplicar una cinta de opciones personalizada al iniciar Access
TOCTitle: Apply a custom ribbon when starting Access
description: Cómo aplicar cintas de opciones personalizadas al abrir una base de datos en Access 2013.
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 10/16/2018
mtps_version: v=office.15
ms.openlocfilehash: 755ff8c5b8c51927de0b212b91f2a332228f0550
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881303"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a><span data-ttu-id="df886-103">Aplicar una cinta de opciones personalizada al iniciar Access</span><span class="sxs-lookup"><span data-stu-id="df886-103">Apply a custom ribbon when starting Access</span></span>

<span data-ttu-id="df886-104">**Se aplica a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="df886-104">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="df886-p101">La cinta usa el marcado XML declarativa basada en texto que simplifica la creación y personalización de la cinta. Con unas pocas líneas de XML, puede crear la interfaz adecuada para el usuario. Access proporciona una gran flexibilidad para personalizar la interfaz de usuario de la cinta. Por ejemplo, el marcado de personalización se puede almacenar en una tabla, insertar en un procedimiento de VBA, almacenar en otra base de datos de Access o vincular desde una hoja de cálculo de Excel. Este tema describe cómo aplicar cintas personalizadas al abrir una base de datos.</span><span class="sxs-lookup"><span data-stu-id="df886-p101">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon. With a few lines of XML, you can create just the right interface for the user. Access provides tremendous flexibility in customizing the ribbon UI. For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet. This topic describes how to apply customized ribbons when opening a database.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="df886-110">Poner a disposición de la personalización de la cinta de opciones XML</span><span class="sxs-lookup"><span data-stu-id="df886-110">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="df886-111">Almacenar código XML de extensibilidad de la cinta de opciones en una tabla</span><span class="sxs-lookup"><span data-stu-id="df886-111">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="df886-p102">Un método que puede usar para que las personalizaciones de la cinta estén disponibles es almacenarlas en una tabla. Si las almacena en una tabla denominada **USysRibbons**, las personalizaciones se pueden implementar sin usar macros o código VBA.</span><span class="sxs-lookup"><span data-stu-id="df886-p102">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="df886-114">**USysRibbons** es una tabla del sistema creada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="df886-114">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="df886-115">La tabla debe crearse utilizando nombres de columna específicos para las personalizaciones de la cinta de opciones para se puedan implementar.</span><span class="sxs-lookup"><span data-stu-id="df886-115">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="df886-116">La tabla siguiente describe la configuración que se utilizará al crear la tabla **USysRibbons**.</span><span class="sxs-lookup"><span data-stu-id="df886-116">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="df886-117">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="df886-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="df886-118">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="df886-118">Data type</span></span></p></th>
<th><p><span data-ttu-id="df886-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="df886-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df886-120"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="df886-120"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="df886-121">Texto</span><span class="sxs-lookup"><span data-stu-id="df886-121">Text</span></span></p></td>
<td><p><span data-ttu-id="df886-122">Contiene el nombre de la Cinta de opciones personalizada que se asociará a esta personalización.</span><span class="sxs-lookup"><span data-stu-id="df886-122">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df886-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="df886-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="df886-124">Memo</span><span class="sxs-lookup"><span data-stu-id="df886-124">Memo</span></span></p></td>
<td><p><span data-ttu-id="df886-125">Contiene el XML (RibbonX) que define la personalización de la cinta de opciones de extensibilidad de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="df886-125">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="df886-126">Cargar el código XML de extensibilidad de la cinta de opciones mediante programación</span><span class="sxs-lookup"><span data-stu-id="df886-126">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="df886-p104">Puede usar el método **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** para cargar las personalizaciones de la cinta mediante programación. Normalmente, para crear y hacer que la cinta esté disponible para la aplicación, primero debe crear un módulo en la base de datos con un procedimiento que llame al método **LoadCustomUI**, pasando el nombre de la cinta y el marcado de personalización XML.</span><span class="sxs-lookup"><span data-stu-id="df886-p104">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="df886-p105">El marcado de personalización XML puede venir de un objeto **Recordset** creado desde una tabla, desde un origen externo a la base de datos como un archivo XML que debe analizar en una cadena, o desde un marcado XML insertado directamente en el procedimiento. Puede crear varias cintas con varias llamadas al método **LoadCustomUI**, pasando un marcado XML diferente siempre que el nombre de cada cinta y el atributo **id** de las pestañas que conforman la cinta sean únicas.</span><span class="sxs-lookup"><span data-stu-id="df886-p105">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="df886-131">Una vez completado el procedimiento, cree una macro AutoExec que llame al procedimiento con la acción RunCode.</span><span class="sxs-lookup"><span data-stu-id="df886-131">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="df886-132">De este modo, cuando se inicia la aplicación, se ejecuta automáticamente el método **LoadCustomUI** y todas las cintas de opciones personalizadas están disponibles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="df886-132">That way, when the application is started, the **LoadCustomUI** method is automatically executed, and all of the custom ribbons are made available to the application.</span></span>

## <a name="apply-customized-ribbons-when-access-starts"></a><span data-ttu-id="df886-133">Aplicar las cintas de opciones personalizadas al iniciar Access</span><span class="sxs-lookup"><span data-stu-id="df886-133">Apply customized ribbons when Access starts</span></span>

<span data-ttu-id="df886-134">Para aplicar una interfaz de usuario personalizada para que esté disponible cuando se inicia la aplicación, use el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="df886-134">To apply a custom UI so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="df886-135">Siga el proceso descrito anteriormente para que las cintas personalizadas estén disponibles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="df886-135">Follow the process described previously to make the customized ribbons available to the application.</span></span>

2.  <span data-ttu-id="df886-136">Cierre y reinicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="df886-136">Close and then restart the application.</span></span>

3.  <span data-ttu-id="df886-137">Elija el **Botón de Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") y, a continuación, elija **Opciones de Access**.</span><span class="sxs-lookup"><span data-stu-id="df886-137">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="df886-138">Elija la opción de **Base de datos actual** y, a continuación, en la sección **Opciones de barra de herramientas y la cinta de opciones** , elija la lista **Nombre de la cinta de opciones** y seleccione una cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="df886-138">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select a ribbon.</span></span>

5.  <span data-ttu-id="df886-p107">Cierre y reinicie la aplicación. Se muestra la interfaz de usuario seleccionada.</span><span class="sxs-lookup"><span data-stu-id="df886-p107">Now close and restart the application. The UI you selected is displayed.</span></span>

> [!NOTE]
> <span data-ttu-id="df886-141">[!NOTA] Para obtener más información sobre la interfaz de usuario de la cinta en otras aplicaciones de Office, consulte [Información general de la cinta de Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="df886-141">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


