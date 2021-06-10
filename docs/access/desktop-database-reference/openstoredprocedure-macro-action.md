---
title: AbrirProcedimientoAlmacenado (acción de macro)
TOCTitle: OpenStoredProcedure macro action
ms:assetid: b14dbb82-7c8a-0ace-e251-46599551a490
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822003(v=office.15)
ms:contentKeyID: 48547142
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm187628
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b972174e4fe7f3c0384b7483e17eb5ceb9e8bc15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288311"
---
# <a name="openstoredprocedure-macro-action"></a><span data-ttu-id="e9974-102">AbrirProcedimientoAlmacenado (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="e9974-102">OpenStoredProcedure macro action</span></span>

<span data-ttu-id="e9974-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9974-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e9974-p101">En un proyecto de Access, puede utilizar la acción **AbrirProcedimientoAlmacenado** para abrir un procedimiento almacenado en la vista Hoja de datos, vista Diseño o Vista preliminar. Esta acción ejecuta el procedimiento almacenado especificado cuando se abre en la vista Hoja de datos. Puede seleccionar el modo de entrada de datos del procedimiento almacenado y restringir los registros que muestra el procedimiento almacenado.</span><span class="sxs-lookup"><span data-stu-id="e9974-p101">In an Access project, you can use the **OpenStoredProcedure** action to open a stored procedure in Datasheet view, stored procedure Design view, or Print Preview. This action runs the named stored procedure when opened in Datasheet view. You can select the data entry mode for the stored procedure and restrict the records that the stored procedure displays.</span></span>

> [!NOTE]
> <span data-ttu-id="e9974-107">Esta acción no se permitirá si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="e9974-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="e9974-108">Configuración</span><span class="sxs-lookup"><span data-stu-id="e9974-108">Setting</span></span>

<span data-ttu-id="e9974-109">La acción **AbrirProcedimientoAlmacenado** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="e9974-109">The **OpenStoredProcedure** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9974-110">Argumento de acción</span><span class="sxs-lookup"><span data-stu-id="e9974-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e9974-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9974-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9974-112"><strong>Nombre del procedimiento</strong></span><span class="sxs-lookup"><span data-stu-id="e9974-112"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="e9974-113">Nombre del procedimiento almacenado que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="e9974-113">The name of the stored procedure to open.</span></span> <span data-ttu-id="e9974-114">El <strong>cuadro Nombre del procedimiento</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todos los procedimientos almacenados en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="e9974-114">The <strong>Procedure Name box</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all stored procedures in the current database.</span></span> <span data-ttu-id="e9974-115">Éste es un argumento requerido.</span><span class="sxs-lookup"><span data-stu-id="e9974-115">This is a required argument.</span></span> <span data-ttu-id="e9974-116">Si ejecuta una macro que contiene la acción <strong>AbrirProcedimientoAlmacenado</strong> en una base de datos de biblioteca, Microsoft Access primero busca el procedimiento almacenado con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos activa.</span><span class="sxs-lookup"><span data-stu-id="e9974-116">If you run a macro containing the <strong>OpenStoredProcedure</strong> action in a library database, Microsoft Access first looks for the stored procedure with this name first in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9974-117"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="e9974-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="e9974-p103">Vista en la que se va a abrir el procedimiento almacenado. Haga clic en <strong>Hoja de datos</strong>, <strong>Diseño</strong>, <strong>Vista preliminar</strong>, <strong>Tabla dinámica</strong> o <strong>Gráfico dinámico</strong> en el cuadro <strong>Vista</strong>. El valor predeterminado es <strong>Hoja de datos</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9974-p103">The view in which the stored procedure will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9974-121"><strong>Modo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="e9974-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="e9974-p104">Modo de entrada de datos del procedimiento almacenado. Se aplica sólo a los procedimientos almacenados que se abren en la vista Hoja de datos. Haga clic en <strong>Agregar</strong> (el usuario puede agregar nuevos registros pero no puede ver ni modificar los existentes), <strong>Modificar</strong> (el usuario puede ver o modificar los registros existentes y agregar otros nuevos) o <strong>Solo lectura</strong> (el usuario sólo puede ver los registros). El valor predeterminado es <strong>Modificar</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9974-p104">The data entry mode for the stored procedure. This applies only to stored procedures opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="e9974-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e9974-126">Remarks</span></span>

<span data-ttu-id="e9974-127">Esta acción es similar a hacer doble clic en el procedimiento almacenado en el panel de navegación, o bien, hacer clic con el botón secundario en el procedimiento almacenado en el panel de navegación y seleccionar el comando deseado.</span><span class="sxs-lookup"><span data-stu-id="e9974-127">This action is similar to double-clicking the stored procedure in the Navigation Pane, or right-clicking the stored procedure in the Navigation Pane and selecting the command you want.</span></span>

<span data-ttu-id="e9974-p105">Si se cambia a la vista Diseño mientras está abierto el procedimiento almacenado, se quita el valor del argumento **Modo de datos** del procedimiento almacenado. Este valor no tiene efecto aunque el usuario vuelva a la vista Hoja de datos.</span><span class="sxs-lookup"><span data-stu-id="e9974-p105">Switching to Design view while the stored procedure is open removes the **Data Mode** argument setting for the stored procedure. This setting is not in effect, even if the user returns to Datasheet view.</span></span>

> [!TIP]
> - <span data-ttu-id="e9974-130">Puede arrastrar un procedimiento almacenado desde el panel de navegación a una fila de acción de macro.</span><span class="sxs-lookup"><span data-stu-id="e9974-130">You can drag a stored procedure from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="e9974-131">De este modo, se crea automáticamente una acción **AbrirProcedimientoAlmacenado** que abre el procedimiento almacenado en la vista Hoja de datos.</span><span class="sxs-lookup"><span data-stu-id="e9974-131">This automatically creates an **OpenStoredProcedure** action that opens the stored procedure in Datasheet view.</span></span>
> - <span data-ttu-id="e9974-132">Si no desea que se muestren los mensajes del sistema que normalmente aparecen al ejecutarse un procedimiento almacenado (los mensajes indican que se trata de un procedimiento almacenado y muestran cuántos registros se verán afectados), puede utilizar la acción **EstablecerAdvertencias** para suprimir la presentación de estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="e9974-132">If you do not want to display the system messages that normally appear when a stored procedure is run (indicating it is a stored procedure and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="e9974-133">Para ejecutar la acción **AbrirProcedimientoAlmacenado** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **OpenStoredProcedure** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="e9974-133">To run the **OpenStoredProcedure** action in a Visual Basic for Applications (VBA) module, use the **OpenStoredProcedure** method of the **DoCmd** object.</span></span>

