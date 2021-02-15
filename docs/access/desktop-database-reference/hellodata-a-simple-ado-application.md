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
# <a name="hellodata-a-simple-ado-application"></a><span data-ttu-id="1aa66-102">HelloData: Una aplicación de ADO simple</span><span class="sxs-lookup"><span data-stu-id="1aa66-102">HelloData: A simple ADO application</span></span>

<span data-ttu-id="1aa66-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1aa66-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1aa66-p101">Para establecer el trabajo de base de una exploración de la biblioteca ADO, considere la opción de utilizar una aplicación ADO simple denominada "HelloData". HelloData ejecuta cada una de las cuatro operaciones principales de ADO (obtener, examinar, editar y actualizar datos). Para centrarse en los conceptos básicos de ADO y evitar la sobrecarga de código, se realiza un mínimo tratamiento de errores en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1aa66-p101">To lay the groundwork for an exploration of the ADO library, consider a simple ADO application called "HelloData." HelloData steps through each of the four major ADO operations (getting, examining, editing, and updating data). In order to focus on the fundamentals of ADO and prevent code clutter, minimal error handling is done in the example.</span></span>

<span data-ttu-id="1aa66-107">La aplicación realiza consultas en la base de datos de ejemplo Neptuno que se incluye con Microsoft SQL Server 2000.</span><span class="sxs-lookup"><span data-stu-id="1aa66-107">The application queries the Northwind sample database that is included with Microsoft SQL Server 2000.</span></span>

<span data-ttu-id="1aa66-108">**Para ejecutar HelloData**</span><span class="sxs-lookup"><span data-stu-id="1aa66-108">**To run HelloData**</span></span>

1.  <span data-ttu-id="1aa66-109">Cree un nuevo proyecto estándar ejecutable de Visual Basic que haga referencia a la biblioteca de ADO 2.5.</span><span class="sxs-lookup"><span data-stu-id="1aa66-109">Create a new Standard Executable Visual Basic Project that references the ADO 2.5 library.</span></span>

2.  <span data-ttu-id="1aa66-110">Cree cuatro botones de comando en la parte superior del formulario, estableciendo las propiedades **Name** y **Caption** en los valores que se muestran en la tabla que figura más abajo.</span><span class="sxs-lookup"><span data-stu-id="1aa66-110">Create four command buttons at the top of the form, setting the **Name** and **Caption** properties to the values shown in the table below.</span></span>

3.  <span data-ttu-id="1aa66-111">Debajo de los botones, agregue un **control cuadrícula de datos de Microsoft** (Msdatgrd.ocx).</span><span class="sxs-lookup"><span data-stu-id="1aa66-111">Below the buttons, add a **Microsoft DataGrid Control** (Msdatgrd.ocx).</span></span> <span data-ttu-id="1aa66-112">El archivo Msdatgrd.ocx viene con Visual Basic y se encuentra en el directorio \\ \\ system32 o \\ winnt \\ system32 de Windows.</span><span class="sxs-lookup"><span data-stu-id="1aa66-112">The Msdatgrd.ocx file comes with Visual Basic and is located in your \\windows\\system32 or \\winnt\\system32 directory.</span></span> <span data-ttu-id="1aa66-113">Para agregar el control cuadrícula de datos al panel de cuadro de herramientas de Visual Basic, seleccione **Componentes** en el menú **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="1aa66-113">To add the DataGrid control to your Visual Basic toolbox pane, select **Components...** from the **Project** menu.</span></span> <span data-ttu-id="1aa66-114">A continuación, compruebe el cuadro situado junto a "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="1aa66-114">Then check the box next to "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" and click **OK**.</span></span> <span data-ttu-id="1aa66-115">Para agregar el control al proyecto, arrastre el control cuadrícula de datos desde el cuadro de herramientas hasta el formulario de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1aa66-115">To add the control to the project, drag the DataGrid control from the Toolbox to the Visual Basic form.</span></span>

4.  <span data-ttu-id="1aa66-p103">Cree un control **cuadro de texto** en el formulario debajo de la cuadrícula y establezca sus propiedades tal como se muestra en la tabla. El formulario debe tener un aspecto similar a la ilustración siguiente cuando haya finalizado.</span><span class="sxs-lookup"><span data-stu-id="1aa66-p103">Create a **TextBox** on the form below the grid and set its properties as shown in the table. The form should look similar to the following figure when you are finished.</span></span>

5.  <span data-ttu-id="1aa66-118">Por último, copie el código enumerado en [HelloData Code](hellodata-code.md) y péguelo en la ventana del editor de código del formulario.</span><span class="sxs-lookup"><span data-stu-id="1aa66-118">Finally, copy the code listed in [HelloData Code](hellodata-code.md) and paste it into the code editor window of the form.</span></span> <span data-ttu-id="1aa66-119">Presione **F5** para que se ejecute el código.</span><span class="sxs-lookup"><span data-stu-id="1aa66-119">Press **F5** to run the code.</span></span>

> [!NOTE]
> <span data-ttu-id="1aa66-p105">[!NOTA] En el ejemplo siguiente y en toda la Guía, se utiliza el identificador de usuario "MyId" con la contraseña "123aBc" para autenticación en el servidor. Debe sustituir estos valores con credenciales de inicio de sesión válidas para su servidor. Sustituya también el valor "MyServer" por el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="1aa66-p105">In the following example, and throughout the guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server. You should substitute these values with valid logon credentials for your server. Also, substitute the "MyServer" value with the name of your server.</span></span>

<span data-ttu-id="1aa66-123">Para obtener una descripción detallada del código, vea [Detalles de HelloData](hellodata-details.md).</span><span class="sxs-lookup"><span data-stu-id="1aa66-123">For a detailed description of the code, see [HelloData Details](hellodata-details.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1aa66-124">Tipo de control</span><span class="sxs-lookup"><span data-stu-id="1aa66-124">Control Type</span></span></p></th>
<th><p><span data-ttu-id="1aa66-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1aa66-125">Property</span></span></p></th>
<th><p><span data-ttu-id="1aa66-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1aa66-126">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1aa66-127">Form</span><span class="sxs-lookup"><span data-stu-id="1aa66-127">Form</span></span></p></td>
<td><p><span data-ttu-id="1aa66-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="1aa66-128">Name</span></span></p></td>
<td><p><span data-ttu-id="1aa66-129">Form1</span><span class="sxs-lookup"><span data-stu-id="1aa66-129">Form1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="1aa66-130">Height</span><span class="sxs-lookup"><span data-stu-id="1aa66-130">Height</span></span></p></td>
<td><p><span data-ttu-id="1aa66-131">6500</span><span class="sxs-lookup"><span data-stu-id="1aa66-131">6500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="1aa66-132">Width</span><span class="sxs-lookup"><span data-stu-id="1aa66-132">Width</span></span></p></td>
<td><p><span data-ttu-id="1aa66-133">6500</span><span class="sxs-lookup"><span data-stu-id="1aa66-133">6500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1aa66-134">Cuadrícula de datos de MS</span><span class="sxs-lookup"><span data-stu-id="1aa66-134">MS DataGrid</span></span></p></td>
<td><p><span data-ttu-id="1aa66-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="1aa66-135">Name</span></span></p></td>
<td><p><span data-ttu-id="1aa66-136">grdDisplay1</span><span class="sxs-lookup"><span data-stu-id="1aa66-136">grdDisplay1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1aa66-137">TextBox</span><span class="sxs-lookup"><span data-stu-id="1aa66-137">TextBox</span></span></p></td>
<td><p><span data-ttu-id="1aa66-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="1aa66-138">Name</span></span></p></td>
<td><p><span data-ttu-id="1aa66-139">txtDisplay1</span><span class="sxs-lookup"><span data-stu-id="1aa66-139">txtDisplay1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="1aa66-140">Multilínea</span><span class="sxs-lookup"><span data-stu-id="1aa66-140">Multiline</span></span></p></td>
<td><p><span data-ttu-id="1aa66-141">true</span><span class="sxs-lookup"><span data-stu-id="1aa66-141">true</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1aa66-142">Botón de comando</span><span class="sxs-lookup"><span data-stu-id="1aa66-142">Command Button</span></span></p></td>
<td><p><span data-ttu-id="1aa66-143">Nombre</span><span class="sxs-lookup"><span data-stu-id="1aa66-143">Name</span></span></p></td>
<td><p><span data-ttu-id="1aa66-144">cmdGetData</span><span class="sxs-lookup"><span data-stu-id="1aa66-144">cmdGetData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="1aa66-145">Caption</span><span class="sxs-lookup"><span data-stu-id="1aa66-145">Caption</span></span></p></td>
<td><p><span data-ttu-id="1aa66-146">Get Data</span><span class="sxs-lookup"><span data-stu-id="1aa66-146">Get Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1aa66-147">Botón de comando</span><span class="sxs-lookup"><span data-stu-id="1aa66-147">Command Button</span></span></p></td>
<td><p><span data-ttu-id="1aa66-148">Nombre</span><span class="sxs-lookup"><span data-stu-id="1aa66-148">Name</span></span></p></td>
<td><p><span data-ttu-id="1aa66-149">cmdExamineData</span><span class="sxs-lookup"><span data-stu-id="1aa66-149">cmdExamineData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="1aa66-150">Caption</span><span class="sxs-lookup"><span data-stu-id="1aa66-150">Caption</span></span></p></td>
<td><p><span data-ttu-id="1aa66-151">Examine Data</span><span class="sxs-lookup"><span data-stu-id="1aa66-151">Examine Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1aa66-152">Botón de comando</span><span class="sxs-lookup"><span data-stu-id="1aa66-152">Command Button</span></span></p></td>
<td><p><span data-ttu-id="1aa66-153">Nombre</span><span class="sxs-lookup"><span data-stu-id="1aa66-153">Name</span></span></p></td>
<td><p><span data-ttu-id="1aa66-154">cmdEditData</span><span class="sxs-lookup"><span data-stu-id="1aa66-154">cmdEditData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="1aa66-155">Caption</span><span class="sxs-lookup"><span data-stu-id="1aa66-155">Caption</span></span></p></td>
<td><p><span data-ttu-id="1aa66-156">Edit Data</span><span class="sxs-lookup"><span data-stu-id="1aa66-156">Edit Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1aa66-157">Botón de comando</span><span class="sxs-lookup"><span data-stu-id="1aa66-157">Command Button</span></span></p></td>
<td><p><span data-ttu-id="1aa66-158">Nombre</span><span class="sxs-lookup"><span data-stu-id="1aa66-158">Name</span></span></p></td>
<td><p><span data-ttu-id="1aa66-159">cmdUpdateData</span><span class="sxs-lookup"><span data-stu-id="1aa66-159">cmdUpdateData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="1aa66-160">Caption</span><span class="sxs-lookup"><span data-stu-id="1aa66-160">Caption</span></span></p></td>
<td><p><span data-ttu-id="1aa66-161">Update Data</span><span class="sxs-lookup"><span data-stu-id="1aa66-161">Update Data</span></span></p></td>
</tr>
</tbody>
</table>



