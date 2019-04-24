---
title: GuardarObjeto (acción de macro)
TOCTitle: SaveObject macro action
ms:assetid: 85716dfc-f76f-ca47-cc40-f8f88162f85a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196789(v=office.15)
ms:contentKeyID: 48546060
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm116962
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cf6fe02616134f864a0e07092951ab9cf49aadbc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308935"
---
# <a name="saveobject-macro-action"></a><span data-ttu-id="ff3ab-102">GuardarObjeto (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="ff3ab-102">SaveObject macro action</span></span>

<span data-ttu-id="ff3ab-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff3ab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ff3ab-p101">Puede usar la acción **GuardarObjeto** para guardar el objeto de Access especificado o el objeto activo si ninguno está especificado. También puede guardar el objeto activo con un nombre nuevo en algunos casos (esto funciona de la misma forma que el comando **Guardar como** en la **Barra de herramientas de acceso rápido**).</span><span class="sxs-lookup"><span data-stu-id="ff3ab-p101">You can use the **SaveObject** action to save either a specified Access object or the active object if none is specified. You can also save the active object with a new name in some cases (this functions the same as the **Save As** command on the **Quick Access Toolbar**).</span></span>

> [!NOTE]
> <span data-ttu-id="ff3ab-106">Esta acción no se permitirá si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="ff3ab-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="ff3ab-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="ff3ab-107">Setting</span></span>

<span data-ttu-id="ff3ab-108">La acción **GuardarObjeto** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="ff3ab-108">The **SaveObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ff3ab-109">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="ff3ab-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ff3ab-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff3ab-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff3ab-111"><strong>Tipo de objeto</strong></span><span class="sxs-lookup"><span data-stu-id="ff3ab-111"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3ab-p102">El tipo de objeto que desea guardar. Haga clic en <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Informe</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong> en la sección <strong>Argumentos de acción</strong> del panel del Generador de macros. Para seleccionar el objeto activo, deje este argumento en blanco. Si selecciona un tipo de objeto en este argumento, debe seleccionar el nombre de un objeto existente en el argumento <strong>Nombre de objeto</strong>.</span><span class="sxs-lookup"><span data-stu-id="ff3ab-p102">The type of object you want to save. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To select the active object, leave this argument blank. If you select an object type in this argument, you must select an existing object's name in the <strong>Object Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff3ab-116"><strong>Nombre del objeto</strong></span><span class="sxs-lookup"><span data-stu-id="ff3ab-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ff3ab-117">El nombre del objeto que desea guardar.</span><span class="sxs-lookup"><span data-stu-id="ff3ab-117">The name of the object to be saved.</span></span> <span data-ttu-id="ff3ab-118">El cuadro <strong>Nombre de objeto</strong> muestra todos los objetos en la base de datos del tipo seleccionado por el argumento <strong>Tipo de objeto</strong>.</span><span class="sxs-lookup"><span data-stu-id="ff3ab-118">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="ff3ab-119">Si deja el argumento <strong>Tipo de objeto</strong> en blanco, puede dejar este argumento en blanco para guardar el objeto activo o, en algunos casos, escribir un nombre nuevo en este argumento para guardar el objeto activo con este nombre.</span><span class="sxs-lookup"><span data-stu-id="ff3ab-119">If you leave the <strong>Object Type</strong> argument blank, you can leave this argument blank to save the active object, or, in some cases, enter a new name in this argument to save the active object with this name.</span></span> <span data-ttu-id="ff3ab-120">Si escribe un nombre nuevo, el nombre debe cumplir con las convenciones de denominación estándar para objetos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ff3ab-120">If you enter a new name, the name must follow the standard naming conventions for Microsoft Access objects.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ff3ab-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ff3ab-121">Remarks</span></span>

<span data-ttu-id="ff3ab-122">La acción **GuardarObjeto** funciona en todos los objetos de base de datos que el usuario puede abrir explícitamente y guardar.</span><span class="sxs-lookup"><span data-stu-id="ff3ab-122">The **SaveObject** action works on all database objects that the user can explicitly open and save.</span></span> <span data-ttu-id="ff3ab-123">El objeto especificado se debe abrir para la acción **GuardarObjeto** para que tenga efecto en el objeto.</span><span class="sxs-lookup"><span data-stu-id="ff3ab-123">The specified object must be open for the **SaveObject** action to have any effect on the object.</span></span> <span data-ttu-id="ff3ab-124">Esta acción tiene el mismo efecto que seleccionar un objeto y guardarlo al hacer clic en **Guardar** en la **Barra de herramientas de acceso rápido**.</span><span class="sxs-lookup"><span data-stu-id="ff3ab-124">This action has the same effect as selecting an object and then saving it by clicking **Save** on the **Quick Access Toolbar**.</span></span> 

<span data-ttu-id="ff3ab-125">Dejar el argumento **Tipo de objeto** en blanco y escribir un nombre nuevo en el argumento **Nombre de objeto** tiene el mismo efecto que hacer clic en **Guardar como** en la **Barra de herramientas de acceso rápido**, y escribir un nombre nuevo para el objeto activo.</span><span class="sxs-lookup"><span data-stu-id="ff3ab-125">Leaving the **Object Type** argument blank and entering a new name in the **Object Name** argument has the same effect as clicking **Save As** on the **Quick Access Toolbar**, and entering a new name for the active object.</span></span> <span data-ttu-id="ff3ab-126">Con la acción **GuardarObjeto** puede especificar un objeto para guardar y ejecutar un comando **Guardar como** desde una macro.</span><span class="sxs-lookup"><span data-stu-id="ff3ab-126">Using the **SaveObject** action enables you to specify an object to save and to perform a **Save As** command from a macro.</span></span>

> [!NOTE]
> <span data-ttu-id="ff3ab-127">No puede utilizar la acción **GuardarObjeto** para guardar cualquiera de los siguientes con un nombre nuevo:</span><span class="sxs-lookup"><span data-stu-id="ff3ab-127">You can't use the **SaveObject** action to save any of the following with a new name:</span></span>
> - <span data-ttu-id="ff3ab-128">Un formulario en la vista formulario o en la vista Hoja de información</span><span class="sxs-lookup"><span data-stu-id="ff3ab-128">A form in Form view or Datasheet view</span></span>
> - <span data-ttu-id="ff3ab-129">Un informe en la vista previa de impresión</span><span class="sxs-lookup"><span data-stu-id="ff3ab-129">A report in Print Preview</span></span>
> - <span data-ttu-id="ff3ab-130">Un módulo</span><span class="sxs-lookup"><span data-stu-id="ff3ab-130">A module</span></span>
> - <span data-ttu-id="ff3ab-131">Una vista de servidor en la vista Hoja de información o vista previa de impresión</span><span class="sxs-lookup"><span data-stu-id="ff3ab-131">A server view in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="ff3ab-132">Una página de acceso a datos en la vista Página</span><span class="sxs-lookup"><span data-stu-id="ff3ab-132">A data access page in Page view</span></span>
> - <span data-ttu-id="ff3ab-133">Una tabla en la vista Hoja de información o vista previa de impresión</span><span class="sxs-lookup"><span data-stu-id="ff3ab-133">A table in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="ff3ab-134">Una consulta en la vista Hoja de información o vista previa de impresión</span><span class="sxs-lookup"><span data-stu-id="ff3ab-134">A query in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="ff3ab-135">Un procedimiento almacenado en la vista Hoja de información o vista previa de impresión</span><span class="sxs-lookup"><span data-stu-id="ff3ab-135">A stored procedure in Datasheet view or Print Preview</span></span>

<span data-ttu-id="ff3ab-136">La acción **GuardarObjeto**, si se lleva a cabo en una macro que se ejecuta en la base de datos activa o en una base de datos de biblioteca, siempre guarda el objeto especificado en la base de datos en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="ff3ab-136">The **SaveObject** action, whether it's carried out in a macro run in the current database or in a library database, always saves the specified object or the active object in the database in which the object was created.</span></span>

<span data-ttu-id="ff3ab-p106">Si guarda el objeto activo con un nombre nuevo, pero el nombre es el mismo que el de un objeto existente de este tipo, un cuadro de diálogo solicita si desea sobrescribir el objeto existente. Si estableció el argumento **Activar advertencias** de la acción **EstablecerAdvertencias** como **No**, el cuadro de diálogo no se muestra y el objeto antiguo se sobrescribe automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ff3ab-p106">If you save the active object with a new name, but the name is the same as the name of an existing object of this type, a dialog box asks if you want to overwrite the existing object. If you've set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box isn't displayed and the old object is automatically overwritten.</span></span>

<span data-ttu-id="ff3ab-139">Para ejecutar la acción **GuardarObjeto** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **Save** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="ff3ab-139">To run the **SaveObject** action in a Visual Basic for Applications (VBA) module, use the **Save** method of the **DoCmd** object.</span></span>

