---
title: 'HelloData: Una aplicación de ADO simple'
TOCTitle: 'HelloData: A simple ADO application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7d9be9b91b3f847516eb3c22aa37e46c8a551d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292023"
---
# <a name="hellodata-a-simple-ado-application"></a><span data-ttu-id="7cc19-102">HelloData: Una aplicación de ADO simple</span><span class="sxs-lookup"><span data-stu-id="7cc19-102">HelloData: A simple ADO application</span></span>

<span data-ttu-id="7cc19-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7cc19-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7cc19-p101">Para establecer el trabajo de base de una exploración de la biblioteca ADO, considere la opción de utilizar una aplicación ADO simple denominada "HelloData". HelloData ejecuta cada una de las cuatro operaciones principales de ADO (obtener, examinar, editar y actualizar datos). Para centrarse en los conceptos básicos de ADO y evitar la sobrecarga de código, se realiza un mínimo tratamiento de errores en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="7cc19-p101">To lay the groundwork for an exploration of the ADO library, consider a simple ADO application called "HelloData." HelloData steps through each of the four major ADO operations (getting, examining, editing, and updating data). In order to focus on the fundamentals of ADO and prevent code clutter, minimal error handling is done in the example.</span></span>

<span data-ttu-id="7cc19-107">La aplicación realiza consultas en la base de datos de ejemplo Neptuno que se incluye con Microsoft SQL Server 2000.</span><span class="sxs-lookup"><span data-stu-id="7cc19-107">The application queries the Northwind sample database that is included with Microsoft SQL Server 2000.</span></span>

<span data-ttu-id="7cc19-108">**Para ejecutar HelloData**</span><span class="sxs-lookup"><span data-stu-id="7cc19-108">**To run HelloData**</span></span>

1.  <span data-ttu-id="7cc19-109">Cree un nuevo proyecto estándar ejecutable de Visual Basic que haga referencia a la biblioteca de ADO 2.5.</span><span class="sxs-lookup"><span data-stu-id="7cc19-109">Create a new Standard Executable Visual Basic Project that references the ADO 2.5 library.</span></span>

2.  <span data-ttu-id="7cc19-110">Cree cuatro botones de comando en la parte superior del formulario, estableciendo las propiedades **Name** y **Caption** en los valores que se muestran en la tabla que figura más abajo.</span><span class="sxs-lookup"><span data-stu-id="7cc19-110">Create four command buttons at the top of the form, setting the **Name** and **Caption** properties to the values shown in the table below.</span></span>

3.  <span data-ttu-id="7cc19-111">Debajo de los botones, agregue un **control cuadrícula de datos de Microsoft** (Msdatgrd.ocx).</span><span class="sxs-lookup"><span data-stu-id="7cc19-111">Below the buttons, add a **Microsoft DataGrid Control** (Msdatgrd.ocx).</span></span> <span data-ttu-id="7cc19-112">El archivo Msdatgrd. ocx incluye Visual Basic y se encuentra en \\el directorio system32\\o \\WinNT\\system32 de Windows.</span><span class="sxs-lookup"><span data-stu-id="7cc19-112">The Msdatgrd.ocx file comes with Visual Basic and is located in your \\windows\\system32 or \\winnt\\system32 directory.</span></span> <span data-ttu-id="7cc19-113">Para agregar el control cuadrícula de datos al panel de cuadro de herramientas de Visual Basic, seleccione **Componentes** en el menú **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="7cc19-113">To add the DataGrid control to your Visual Basic toolbox pane, select **Components...** from the **Project** menu.</span></span> <span data-ttu-id="7cc19-114">A continuación, compruebe el cuadro situado junto a "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7cc19-114">Then check the box next to "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" and click **OK**.</span></span> <span data-ttu-id="7cc19-115">Para agregar el control al proyecto, arrastre el control cuadrícula de datos desde el cuadro de herramientas hasta el formulario de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7cc19-115">To add the control to the project, drag the DataGrid control from the Toolbox to the Visual Basic form.</span></span>

4.  <span data-ttu-id="7cc19-p103">Cree un control **cuadro de texto** en el formulario debajo de la cuadrícula y establezca sus propiedades tal como se muestra en la tabla. El formulario debe tener un aspecto similar a la ilustración siguiente cuando haya finalizado.</span><span class="sxs-lookup"><span data-stu-id="7cc19-p103">Create a **TextBox** on the form below the grid and set its properties as shown in the table. The form should look similar to the following figure when you are finished.</span></span>

5.  <span data-ttu-id="7cc19-118">Por último, copie el código que se muestra en el [código HelloData](hellodata-code.md) y péguelo en la ventana del editor de código del formulario.</span><span class="sxs-lookup"><span data-stu-id="7cc19-118">Finally, copy the code listed in [HelloData Code](hellodata-code.md) and paste it into the code editor window of the form.</span></span> <span data-ttu-id="7cc19-119">Presione **F5** para que se ejecute el código.</span><span class="sxs-lookup"><span data-stu-id="7cc19-119">Press **F5** to run the code.</span></span>

> [!NOTE]
> <span data-ttu-id="7cc19-p105">[!NOTA] En el ejemplo siguiente y en toda la Guía, se utiliza el identificador de usuario "MyId" con la contraseña "123aBc" para autenticación en el servidor. Debe sustituir estos valores con credenciales de inicio de sesión válidas para su servidor. Sustituya también el valor "MyServer" por el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="7cc19-p105">In the following example, and throughout the guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server. You should substitute these values with valid logon credentials for your server. Also, substitute the "MyServer" value with the name of your server.</span></span>

<span data-ttu-id="7cc19-123">Para obtener una descripción detallada del código, vea [HelloData](hellodata-details.md)details.</span><span class="sxs-lookup"><span data-stu-id="7cc19-123">For a detailed description of the code, see [HelloData Details](hellodata-details.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7cc19-124">Tipo de control</span><span class="sxs-lookup"><span data-stu-id="7cc19-124">Control Type</span></span></p></th>
<th><p><span data-ttu-id="7cc19-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7cc19-125">Property</span></span></p></th>
<th><p><span data-ttu-id="7cc19-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7cc19-126">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7cc19-127">Formulario</span><span class="sxs-lookup"><span data-stu-id="7cc19-127">Form</span></span></p></td>
<td><p><span data-ttu-id="7cc19-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="7cc19-128">Name</span></span></p></td>
<td><p><span data-ttu-id="7cc19-129">Form1</span><span class="sxs-lookup"><span data-stu-id="7cc19-129">Form1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="7cc19-130">Height</span><span class="sxs-lookup"><span data-stu-id="7cc19-130">Height</span></span></p></td>
<td><p><span data-ttu-id="7cc19-131">6500</span><span class="sxs-lookup"><span data-stu-id="7cc19-131">6500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="7cc19-132">Width</span><span class="sxs-lookup"><span data-stu-id="7cc19-132">Width</span></span></p></td>
<td><p><span data-ttu-id="7cc19-133">6500</span><span class="sxs-lookup"><span data-stu-id="7cc19-133">6500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cc19-134">Cuadrícula de datos de MS</span><span class="sxs-lookup"><span data-stu-id="7cc19-134">MS DataGrid</span></span></p></td>
<td><p><span data-ttu-id="7cc19-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="7cc19-135">Name</span></span></p></td>
<td><p><span data-ttu-id="7cc19-136">grdDisplay1</span><span class="sxs-lookup"><span data-stu-id="7cc19-136">grdDisplay1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cc19-137">TextBox</span><span class="sxs-lookup"><span data-stu-id="7cc19-137">TextBox</span></span></p></td>
<td><p><span data-ttu-id="7cc19-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="7cc19-138">Name</span></span></p></td>
<td><p><span data-ttu-id="7cc19-139">txtDisplay1</span><span class="sxs-lookup"><span data-stu-id="7cc19-139">txtDisplay1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="7cc19-140">Lambda</span><span class="sxs-lookup"><span data-stu-id="7cc19-140">Multiline</span></span></p></td>
<td><p><span data-ttu-id="7cc19-141">true</span><span class="sxs-lookup"><span data-stu-id="7cc19-141">true</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cc19-142">Botón de comando</span><span class="sxs-lookup"><span data-stu-id="7cc19-142">Command Button</span></span></p></td>
<td><p><span data-ttu-id="7cc19-143">Nombre</span><span class="sxs-lookup"><span data-stu-id="7cc19-143">Name</span></span></p></td>
<td><p><span data-ttu-id="7cc19-144">cmdGetData</span><span class="sxs-lookup"><span data-stu-id="7cc19-144">cmdGetData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="7cc19-145">Caption</span><span class="sxs-lookup"><span data-stu-id="7cc19-145">Caption</span></span></p></td>
<td><p><span data-ttu-id="7cc19-146">Get Data</span><span class="sxs-lookup"><span data-stu-id="7cc19-146">Get Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cc19-147">Botón de comando</span><span class="sxs-lookup"><span data-stu-id="7cc19-147">Command Button</span></span></p></td>
<td><p><span data-ttu-id="7cc19-148">Nombre</span><span class="sxs-lookup"><span data-stu-id="7cc19-148">Name</span></span></p></td>
<td><p><span data-ttu-id="7cc19-149">cmdExamineData</span><span class="sxs-lookup"><span data-stu-id="7cc19-149">cmdExamineData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="7cc19-150">Caption</span><span class="sxs-lookup"><span data-stu-id="7cc19-150">Caption</span></span></p></td>
<td><p><span data-ttu-id="7cc19-151">Examine Data</span><span class="sxs-lookup"><span data-stu-id="7cc19-151">Examine Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cc19-152">Botón de comando</span><span class="sxs-lookup"><span data-stu-id="7cc19-152">Command Button</span></span></p></td>
<td><p><span data-ttu-id="7cc19-153">Nombre</span><span class="sxs-lookup"><span data-stu-id="7cc19-153">Name</span></span></p></td>
<td><p><span data-ttu-id="7cc19-154">cmdEditData</span><span class="sxs-lookup"><span data-stu-id="7cc19-154">cmdEditData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="7cc19-155">Caption</span><span class="sxs-lookup"><span data-stu-id="7cc19-155">Caption</span></span></p></td>
<td><p><span data-ttu-id="7cc19-156">Edit Data</span><span class="sxs-lookup"><span data-stu-id="7cc19-156">Edit Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cc19-157">Botón de comando</span><span class="sxs-lookup"><span data-stu-id="7cc19-157">Command Button</span></span></p></td>
<td><p><span data-ttu-id="7cc19-158">Nombre</span><span class="sxs-lookup"><span data-stu-id="7cc19-158">Name</span></span></p></td>
<td><p><span data-ttu-id="7cc19-159">cmdUpdateData</span><span class="sxs-lookup"><span data-stu-id="7cc19-159">cmdUpdateData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="7cc19-160">Caption</span><span class="sxs-lookup"><span data-stu-id="7cc19-160">Caption</span></span></p></td>
<td><p><span data-ttu-id="7cc19-161">Update Data</span><span class="sxs-lookup"><span data-stu-id="7cc19-161">Update Data</span></span></p></td>
</tr>
</tbody>
</table>



