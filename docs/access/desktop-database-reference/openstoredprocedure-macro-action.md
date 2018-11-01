---
title: AbrirProcedimientoAlmacenado (acción de macro)
TOCTitle: OpenStoredProcedure Macro Action
ms:assetid: b14dbb82-7c8a-0ace-e251-46599551a490
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822003(v=office.15)
ms:contentKeyID: 48547142
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm187628
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 52d7d6c54913511ab593ee77d374ed55984ed40b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883256"
---
# <a name="openstoredprocedure-macro-action"></a><span data-ttu-id="b2323-102">AbrirProcedimientoAlmacenado (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="b2323-102">OpenStoredProcedure Macro Action</span></span>


<span data-ttu-id="b2323-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2323-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b2323-p101">En un proyecto de Access, puede utilizar la acción **AbrirProcedimientoAlmacenado** para abrir un procedimiento almacenado en la vista Hoja de datos, vista Diseño o Vista preliminar. Esta acción ejecuta el procedimiento almacenado especificado cuando se abre en la vista Hoja de datos. Puede seleccionar el modo de entrada de datos del procedimiento almacenado y restringir los registros que muestra el procedimiento almacenado.</span><span class="sxs-lookup"><span data-stu-id="b2323-p101">In an Access project, you can use the **OpenStoredProcedure** action to open a stored procedure in Datasheet view, stored procedure Design view, or Print Preview. This action runs the named stored procedure when opened in Datasheet view. You can select the data entry mode for the stored procedure and restrict the records that the stored procedure displays.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b2323-p102">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.</span><span class="sxs-lookup"><span data-stu-id="b2323-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="b2323-109">Configuración</span><span class="sxs-lookup"><span data-stu-id="b2323-109">Setting</span></span>

<span data-ttu-id="b2323-110">La acción **AbrirProcedimientoAlmacenado** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="b2323-110">The **OpenStoredProcedure** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b2323-111">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="b2323-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b2323-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2323-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2323-113"><strong>Nombre del procedimiento</strong></span><span class="sxs-lookup"><span data-stu-id="b2323-113"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b2323-114">El nombre del procedimiento almacenado para abrir.</span><span class="sxs-lookup"><span data-stu-id="b2323-114">The name of the stored procedure to open.</span></span> <span data-ttu-id="b2323-115">El cuadro <strong>Nombre del procedimiento</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todos los procedimientos almacenados en la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="b2323-115">The <strong>Procedure Name box</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all stored procedures in the current database.</span></span> <span data-ttu-id="b2323-116">Este argumento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b2323-116">This is a required argument.</span></span> <span data-ttu-id="b2323-117">Si ejecuta una macro que contiene la acción <strong>AbrirProcedimientoAlmacenado</strong> en una base de datos de biblioteca, Microsoft Access primero busca el procedimiento almacenado con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos activa.</span><span class="sxs-lookup"><span data-stu-id="b2323-117">If you run a macro containing the <strong>OpenStoredProcedure</strong> action in a library database, Microsoft Access first looks for the stored procedure with this name first in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2323-118"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="b2323-118"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="b2323-p104">Vista en la que se va a abrir el procedimiento almacenado. Haga clic en <strong>Hoja de datos</strong>, <strong>Diseño</strong>, <strong>Vista preliminar</strong>, <strong>Tabla dinámica</strong> o <strong>Gráfico dinámico</strong> en el cuadro <strong>Vista</strong>. El valor predeterminado es <strong>Hoja de datos</strong>.</span><span class="sxs-lookup"><span data-stu-id="b2323-p104">The view in which the stored procedure will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2323-122"><strong>Modo de datos</strong></span><span class="sxs-lookup"><span data-stu-id="b2323-122"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="b2323-p105">Modo de entrada de datos del procedimiento almacenado. Se aplica sólo a los procedimientos almacenados que se abren en la vista Hoja de datos. Haga clic en <strong>Agregar</strong> (el usuario puede agregar nuevos registros pero no puede ver ni modificar los existentes), <strong>Modificar</strong> (el usuario puede ver o modificar los registros existentes y agregar otros nuevos) o <strong>Solo lectura</strong> (el usuario sólo puede ver los registros). El valor predeterminado es <strong>Modificar</strong>.</span><span class="sxs-lookup"><span data-stu-id="b2323-p105">The data entry mode for the stored procedure. This applies only to stored procedures opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b2323-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b2323-127">Remarks</span></span>

<span data-ttu-id="b2323-128">Esta acción es similar a hacer doble clic en el procedimiento almacenado en el panel de navegación, o bien, hacer clic con el botón secundario en el procedimiento almacenado en el panel de navegación y seleccionar el comando deseado.</span><span class="sxs-lookup"><span data-stu-id="b2323-128">This action is similar to double-clicking the stored procedure in the Navigation Pane, or right-clicking the stored procedure in the Navigation Pane and selecting the command you want.</span></span>

<span data-ttu-id="b2323-p106">Si se cambia a la vista Diseño mientras está abierto el procedimiento almacenado, se quita el valor del argumento **Modo de datos** del procedimiento almacenado. Este valor no tiene efecto aunque el usuario vuelva a la vista Hoja de datos.</span><span class="sxs-lookup"><span data-stu-id="b2323-p106">Switching to Design view while the stored procedure is open removes the **Data Mode** argument setting for the stored procedure. This setting is not in effect, even if the user returns to Datasheet view.</span></span>


> [!TIP]
> <P></P>
> <UL>
> <LI>
> <P><span data-ttu-id="b2323-131">Puede arrastrar un procedimiento almacenado desde el panel de navegación a una fila de la acción de macro.</span><span class="sxs-lookup"><span data-stu-id="b2323-131">You can drag a stored procedure from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="b2323-132">Esto crea automáticamente una acción <STRONG>AbrirProcedimientoAlmacenado</STRONG> que abre el procedimiento almacenado en la vista Hoja de datos.</span><span class="sxs-lookup"><span data-stu-id="b2323-132">This automatically creates an <STRONG>OpenStoredProcedure</STRONG> action that opens the stored procedure in Datasheet view.</span></span></P>
> <LI>
> <P><span data-ttu-id="b2323-133">
> 						Si no desea que se muestren los mensajes del sistema que normalmente aparecen al ejecutarse un procedimiento almacenado (los mensajes indican que se trata de un procedimiento almacenado y muestran cuántos registros se verán afectados), puede utilizar la acción <STRONG>EstablecerAdvertencias</STRONG> para suprimir la presentación de estos mensajes.
</span><span class="sxs-lookup"><span data-stu-id="b2323-133">If you do not want to display the system messages that normally appear when a stored procedure is run (indicating it is a stored procedure and showing how many records will be affected), you can use the <STRONG>SetWarning</STRONG> action to suppress the display of these messages.</span></span></P></LI></UL>
<P></P>



<span data-ttu-id="b2323-134">Para ejecutar la acción **AbrirProcedimientoAlmacenado** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **OpenStoredProcedure** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="b2323-134">To run the **OpenStoredProcedure** action in a Visual Basic for Applications (VBA) module, use the **OpenStoredProcedure** method of the **DoCmd** object.</span></span>

