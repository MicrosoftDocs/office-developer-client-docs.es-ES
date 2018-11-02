---
title: IrARegistro (acción de macro)
TOCTitle: GoToRecord macro action
ms:assetid: 76f936de-739b-63be-9b28-5b0e111408e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196037(v=office.15)
ms:contentKeyID: 48545712
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm58124
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 90d50ce1f1435d38fdfe1ed11e76b49c212b87b3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922457"
---
# <a name="gotorecord-macro-action"></a><span data-ttu-id="09951-102">IrARegistro (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="09951-102">GoToRecord macro action</span></span>


<span data-ttu-id="09951-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="09951-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09951-104">Puede usar la acción **IrARegistro** para convertir el registro especificado en el registro activo de una tabla abierta, un formulario abierto o el conjunto de resultados de una consulta abierta.</span><span class="sxs-lookup"><span data-stu-id="09951-104">You can use the **GoToRecord** action to make the specified record the current record in an open table, form, or query result set.</span></span>

## <a name="setting"></a><span data-ttu-id="09951-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="09951-105">Setting</span></span>

<span data-ttu-id="09951-106">La acción **IrARegistro** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="09951-106">The **GoToRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09951-107">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="09951-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="09951-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="09951-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09951-109"><strong>Tipo de objeto</strong></span><span class="sxs-lookup"><span data-stu-id="09951-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="09951-p101">Tipo de objeto que contiene el registro que se desea convertir en registro activo. Haga clic en <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Vista de servidor</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Deje este argumento en blanco para seleccionar el objeto activo.</span><span class="sxs-lookup"><span data-stu-id="09951-p101">The type of object that contains the record you want to make current. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09951-113"><strong>Nombre del objeto</strong></span><span class="sxs-lookup"><span data-stu-id="09951-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="09951-p102">Nombre del objeto que contiene el registro que se desea convertir en registro activo. El cuadro <strong>Nombre del objeto</strong> muestra todos los objetos de la base de datos activa que sean del tipo seleccionado por el argumento <strong>Tipo de objeto</strong>. Si deja en blanco el argumento <strong>Tipo de objeto</strong>, deje también en blanco este argumento.</span><span class="sxs-lookup"><span data-stu-id="09951-p102">The name of the object that contains the record you want to make the current record. The <strong>Object Name</strong> box shows all objects in the current database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09951-117"><strong>Record</strong></span><span class="sxs-lookup"><span data-stu-id="09951-117"><strong>Record</strong></span></span></p></td>
<td><p><span data-ttu-id="09951-p103">Registro que se va a convertir en registro activo. Haga clic en <strong>Anterior</strong>, <strong>Siguiente</strong>, <strong>Primero</strong>, <strong>Último</strong>, <strong>Ir a</strong> o <strong>Nuevo</strong> en el cuadro <strong>Registro</strong>. El valor predeterminado es <strong>Siguiente</strong>.</span><span class="sxs-lookup"><span data-stu-id="09951-p103">The record to make the current record. Click <strong>Previous</strong>, <strong>Next</strong>, <strong>First</strong>, <strong>Last</strong>, <strong>Go To</strong>, or <strong>New</strong> in the <strong>Record</strong> box. The default is <strong>Next</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09951-121"><strong>Offset</strong></span><span class="sxs-lookup"><span data-stu-id="09951-121"><strong>Offset</strong></span></span></p></td>
<td><p><span data-ttu-id="09951-122">Un número entero o una expresión que da como resultado un número entero.</span><span class="sxs-lookup"><span data-stu-id="09951-122">An integer or expression that evaluates to an integer.</span></span> <span data-ttu-id="09951-123">Una expresión debe ir precedida de un signo igual (<strong>=</strong>).</span><span class="sxs-lookup"><span data-stu-id="09951-123">An expression must be preceded by an equal sign (<strong>=</strong>).</span></span> <span data-ttu-id="09951-124">Este argumento especifica el registro para hacer que sea el registro actual.</span><span class="sxs-lookup"><span data-stu-id="09951-124">This argument specifies the record to make the current record.</span></span> <span data-ttu-id="09951-125">Puede usar el argumento <strong>desplazamiento</strong> de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="09951-125">You can use the <strong>Offset</strong> argument in two ways:</span></span></p>
<ul>
<li><p><span data-ttu-id="09951-126">Cuando el valor del argumento <strong>Registro</strong> es <strong>Siguiente</strong> o <strong>Anterior</strong>, Microsoft Office Access 2007 se mueve hacia delante o hacia atrás el número de registros especificado en el argumento <strong>Desplazamiento</strong>.</span><span class="sxs-lookup"><span data-stu-id="09951-126">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="09951-p105">Cuando el valor del argumento <strong>Registro</strong> es <strong>Ir a</strong>, Access se desplaza al registro que tenga el mismo número que el argumento <strong>Desplazamiento</strong>. El número de registro se muestra en el cuadro de número de registro situado en la parte inferior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="09951-p105">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument. The record number is shown in the record number box at the bottom of the window.</span></span></p></li>
</ul>

> [!NOTE]
> <P><span data-ttu-id="09951-p106">Si se usa el valor <STRONG>Primero</STRONG>, <STRONG>Último</STRONG> o <STRONG>Nuevo</STRONG> para el argumento <STRONG>Registro</STRONG>, Access omite el argumento <STRONG>Desplazamiento</STRONG>. Si se especifica para el argumento <STRONG>Desplazamiento</STRONG> un valor excesivo, Access muestra un mensaje de error. No se pueden especificar números negativos para el argumento <STRONG>Desplazamiento</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="09951-p106">If you use the <STRONG>First</STRONG>, <STRONG>Last</STRONG>, or <STRONG>New</STRONG> setting for the <STRONG>Record</STRONG> argument, Access ignores the <STRONG>Offset</STRONG> argument. If you enter an <STRONG>Offset</STRONG> argument that is too large, Access displays an error message. You can't enter negative numbers for the <STRONG>Offset</STRONG> argument.</span></span></P>


<p></p>
<ul>
<li><p><span data-ttu-id="09951-132">Cuando el valor del argumento <strong>Registro</strong> es <strong>Siguiente</strong> o <strong>Anterior</strong>, Microsoft Office Access 2007 se mueve hacia delante o hacia atrás el número de registros especificado en el argumento <strong>Desplazamiento</strong>.</span><span class="sxs-lookup"><span data-stu-id="09951-132">When the <strong>Record</strong> argument is <strong>Next</strong> or <strong>Previous</strong>, Microsoft Office Access 2007 moves the number of records forward or backward specified in the <strong>Offset</strong> argument.</span></span></p></li>
<li><p><span data-ttu-id="09951-p107">Cuando el valor del argumento <strong>Registro</strong> es <strong>Ir a</strong>, Access se desplaza al registro que tenga el mismo número que el argumento <strong>Desplazamiento</strong>. El número de registro se muestra en el cuadro de número de registro situado en la parte inferior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="09951-p107">When the <strong>Record</strong> argument is <strong>Go To</strong>, Access moves to the record with the number equal to the <strong>Offset</strong> argument. The record number is shown in the record number box at the bottom of the window.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="09951-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09951-135">Remarks</span></span>

<span data-ttu-id="09951-136">Si el enfoque está en un control determinado de un registro, esta acción lo deja en el mismo control del nuevo registro.</span><span class="sxs-lookup"><span data-stu-id="09951-136">If the focus is in a particular control in a record, this action leaves it in the same control for the new record.</span></span>

<span data-ttu-id="09951-137">Se puede usar el valor **Nuevo** para el argumento **Registro** para ir al registro en blanco situado al final de un formulario o una tabla de manera que se puedan escribir nuevos datos.</span><span class="sxs-lookup"><span data-stu-id="09951-137">You can use the **New** setting for the **Record** argument to move to the blank record at the end of a form or table so you can enter new data.</span></span>

<span data-ttu-id="09951-p108">Esta acción es similar a hacer clic en la flecha situada debajo del botón **Buscar** en la ficha **Inicio** y, a continuación, hacer clic en **Ir a**. Los subcomandos **Primero**, **Último**, **Siguiente**, **Anterior** y **Nuevo registro** del comando **Ir a** tienen el mismo efecto en el objeto seleccionado que los valores **Primero**, **Último**, **Siguiente**, **Anterior** y **Nuevo** del argumento **Registro**. Asimismo, puede moverse a registros mediante los botones de navegación situados en la parte inferior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="09951-p108">This action is similar to clicking the arrow below the **Find** button on the **Home** tab and then clicking **Go To**. The **First**, **Last**, **Next**, **Previous**, and **New Record** subcommands of the **Go To** command have the same effect on the selected object as the **First**, **Last**, **Next**, **Previous**, and **New** settings for the **Record** argument. You can also move to records by using the navigation buttons at the bottom of the window.</span></span>

<span data-ttu-id="09951-141">Puede usar la acción **IrARegistro** para convertir un registro de un formulario oculto en registro activo si especifica el formulario oculto en los argumentos **Tipo de objeto** y **Nombre del objeto**.</span><span class="sxs-lookup"><span data-stu-id="09951-141">You can use the **GoToRecord** action to make a record on a hidden form the current record if you specify the hidden form in the **Object Type** and **Object Name** arguments.</span></span>

<span data-ttu-id="09951-142">Para ejecutar la acción **IrARegistro** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **GoToRecord** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="09951-142">To run the **GoToRecord** action in a Visual Basic for Applications (VBA) module, use the **GoToRecord** method of the **DoCmd** object.</span></span>

