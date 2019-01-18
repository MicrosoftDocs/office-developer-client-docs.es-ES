---
title: Eliminación previa (evento de macro)
TOCTitle: Before Delete macro event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2b2a4f978a4af2ba79cab7807f0142d35d7d30c7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705004"
---
# <a name="before-delete-macro-event"></a><span data-ttu-id="cb9b5-102">Eliminación previa (evento de macro)</span><span class="sxs-lookup"><span data-stu-id="cb9b5-102">Before Delete macro event</span></span>

<span data-ttu-id="cb9b5-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb9b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cb9b5-104">El evento **Eliminación previa** se produce cuando se elimina un registro, pero antes de confirmar el cambio.</span><span class="sxs-lookup"><span data-stu-id="cb9b5-104">The **Before Delete** event occurs when a record is deleted, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="cb9b5-105">[!NOTA] El evento **Eliminación previa** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="cb9b5-105">The **Before Delete** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb9b5-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb9b5-106">Remarks</span></span>

<span data-ttu-id="cb9b5-107">Utilice el evento **Eliminación previa** para realizar cualquier acción que desee que ocurra antes de eliminar un registro.</span><span class="sxs-lookup"><span data-stu-id="cb9b5-107">Use the **Before Delete** event to perform any actions that you want to occur before a record is deleted.</span></span> <span data-ttu-id="cb9b5-108">**Cambio previo** se suele utilizar para realizar la validación y para provocar mensajes de error personalizados.</span><span class="sxs-lookup"><span data-stu-id="cb9b5-108">The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="cb9b5-109">Puede tener acceso a un valor en el registro que se va a eliminar mediante el uso de la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="cb9b5-109">You can access a value in the record to be deleted by using the following syntax:</span></span>

`[Old].[Field Name]`

<span data-ttu-id="cb9b5-110">Por ejemplo, para tener acceso al valor del campo QuantityInStock en el registro que se va a eliminar, use la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="cb9b5-110">For example, to access the value of the QuantityInStock field in the record to be deleted, use the following syntax:</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="cb9b5-111">Cuando finaliza el evento **Eliminación previa**, se eliminan permanentemente los valores contenidos en el registro que hay que eliminar.</span><span class="sxs-lookup"><span data-stu-id="cb9b5-111">The values contained in the record to be deleted are deleted permanently when the **Before Delete** event ends.</span></span>

<span data-ttu-id="cb9b5-112">Puede cancelar el evento **Eliminación previa** mediante la acción **ProvocarError**.</span><span class="sxs-lookup"><span data-stu-id="cb9b5-112">You can cancel the **Before Delete** event by using the **RaiseError** action.</span></span> <span data-ttu-id="cb9b5-113">Cuando se produce un error, se descartan los cambios incluidos en el evento **Antes de eliminar** .</span><span class="sxs-lookup"><span data-stu-id="cb9b5-113">When an error is raised, the changes contained in the **Before Delete** event are discarded.</span></span>

<span data-ttu-id="cb9b5-114">La siguiente tabla enumera los comandos de macro que pueden utilizarse en el evento **Eliminación previa**.</span><span class="sxs-lookup"><span data-stu-id="cb9b5-114">The following table lists macro commands that can be used in the **Before Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb9b5-115">Tipo de comando</span><span class="sxs-lookup"><span data-stu-id="cb9b5-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="cb9b5-116">Comando</span><span class="sxs-lookup"><span data-stu-id="cb9b5-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb9b5-117">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="cb9b5-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="cb9b5-118"><a href="comment-macro-statement.md">Instrucción de macro de comentario</a></span><span class="sxs-lookup"><span data-stu-id="cb9b5-118"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb9b5-119">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="cb9b5-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="cb9b5-120"><a href="group-macro-statement.md">Instrucción de macro de grupo</a></span><span class="sxs-lookup"><span data-stu-id="cb9b5-120"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb9b5-121">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="cb9b5-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="cb9b5-122"><a href="if-then-else-macro-block.md">If... A continuación... Bloque de macro Else</a></span><span class="sxs-lookup"><span data-stu-id="cb9b5-122"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb9b5-123">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="cb9b5-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="cb9b5-124"><a href="lookuprecord-data-block.md">Acción de macro BuscarRegistro</a></span><span class="sxs-lookup"><span data-stu-id="cb9b5-124"><a href="lookuprecord-data-block.md">LookupRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb9b5-125">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="cb9b5-125">Data Action</span></span></p></td>
<td><p><span data-ttu-id="cb9b5-126"><a href="clearmacroerror-macro-action.md">Acción de macro BorrarErrorDeMacro</a></span><span class="sxs-lookup"><span data-stu-id="cb9b5-126"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb9b5-127">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="cb9b5-127">Data Action</span></span></p></td>
<td><p><span data-ttu-id="cb9b5-128"><a href="onerror-macro-action.md">Acción de macro AlOcurrirError</a></span><span class="sxs-lookup"><span data-stu-id="cb9b5-128"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb9b5-129">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="cb9b5-129">Data Action</span></span></p></td>
<td><p><span data-ttu-id="cb9b5-130"><a href="raiseerror-macro-action.md">Acción de macro Provocarerror</a></span><span class="sxs-lookup"><span data-stu-id="cb9b5-130"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb9b5-131">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="cb9b5-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="cb9b5-132"><a href="setlocalvar-macro-action.md">Acción de macro EstablecerVariableLocal</a></span><span class="sxs-lookup"><span data-stu-id="cb9b5-132"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb9b5-133">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="cb9b5-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="cb9b5-134"><a href="stopmacro-macro-action.md">Acción de macro DetenerMacro</a></span><span class="sxs-lookup"><span data-stu-id="cb9b5-134"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cb9b5-135">Para crear una macro de datos que capture el evento **Eliminación previa**, utilice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="cb9b5-135">To create a Data macro that captures the **Before Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="cb9b5-136">Abra la tabla en la que desee capturar el evento **Eliminación previa**.</span><span class="sxs-lookup"><span data-stu-id="cb9b5-136">Open the table for which you want to capture the **Before Delete** event.</span></span>

2.  <span data-ttu-id="cb9b5-137">En la ficha **tabla** , en el grupo **Antes de eventos** , seleccione **Antes de eliminar**.</span><span class="sxs-lookup"><span data-stu-id="cb9b5-137">On the **Table** tab, in the **Before Events** group, select **Before Delete**.</span></span>

