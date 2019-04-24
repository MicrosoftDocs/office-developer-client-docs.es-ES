---
title: QuitarVariableTemporal (acción de macro)
TOCTitle: RemoveTempVar macro action
ms:assetid: 7bcc5010-3e30-ecef-2c5d-a35e73c8e325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196352(v=office.15)
ms:contentKeyID: 48545822
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm147125
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5051cfd74f2a745ee430f2ed8a20445d2f9965f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306758"
---
# <a name="removetempvar-macro-action"></a><span data-ttu-id="64b6f-102">QuitarVariableTemporal (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="64b6f-102">RemoveTempVar macro action</span></span>


<span data-ttu-id="64b6f-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64b6f-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="64b6f-104">Puede usar la acción **QuitarVariableTemporal** para quitar una sola variable temporal creada mediante la acción **DefinirVariableTemporal**.</span><span class="sxs-lookup"><span data-stu-id="64b6f-104">You can use the **RemoveTempVar** action to remove a single temporary variable that you created by using the **SetTempVar** action.</span></span>

## <a name="setting"></a><span data-ttu-id="64b6f-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="64b6f-105">Setting</span></span>

<span data-ttu-id="64b6f-106">La acción **QuitarVariableTemporal** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="64b6f-106">The **RemoveTempVar** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64b6f-107">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="64b6f-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="64b6f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="64b6f-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64b6f-109"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="64b6f-109"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="64b6f-110">Especifique el nombre de la variable temporal que desee quitar.</span><span class="sxs-lookup"><span data-stu-id="64b6f-110">Enter the name of the temporary variable you want to remove.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="64b6f-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="64b6f-111">Remarks</span></span>

  - <span data-ttu-id="64b6f-p101">Puede haber hasta 255 variables temporales definidas a la vez. Si no se quita una variable temporal, se mantiene en la memoria hasta que se cierre la base de datos. Se recomienda quitar las variables temporales cuando termine de usarlas.</span><span class="sxs-lookup"><span data-stu-id="64b6f-p101">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database. It is a good practice to remove temporary variables when you are finished using them.</span></span>

  - <span data-ttu-id="64b6f-115">Access quita automáticamente todas las variables temporales cuando se cierra la base de datos o el proyecto.</span><span class="sxs-lookup"><span data-stu-id="64b6f-115">Access automatically removes all temporary variables when you close the database or project.</span></span>

  - <span data-ttu-id="64b6f-p102">Si está mal escrito el nombre de la variable que se desea quitar, Access no muestra ningún error. La variable en cuestión permanecerá en la memoria hasta que se cierre la base de datos.</span><span class="sxs-lookup"><span data-stu-id="64b6f-p102">If you misspell the name of the variable to be removed, Access does not display an error. The variable you wanted to remove will remain in memory until you close the database.</span></span>

  - <span data-ttu-id="64b6f-118">Si ha creado más de una variable temporal y desea quitarlas todas a la vez, use la acción **QuitarTodasLasVariablesTemporales**.</span><span class="sxs-lookup"><span data-stu-id="64b6f-118">If you have created more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

  - <span data-ttu-id="64b6f-119">Para ejecutar la acción **QuitarVariableTemporal** en un módulo de VBA, use el método **Remove** del objeto **TempVars**.</span><span class="sxs-lookup"><span data-stu-id="64b6f-119">To run the **RemoveTempVar** action in a VBA module, use the **Remove** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="64b6f-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="64b6f-120">Example</span></span>

<span data-ttu-id="64b6f-121">En la siguiente macro se muestra cómo crear una variable temporal, cómo usarla en una condición y un cuadro de mensaje y, a continuación, cómo quitarla mediante la acción **QuitarVariableTemporal**.</span><span class="sxs-lookup"><span data-stu-id="64b6f-121">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveTempVar** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64b6f-122">Condición</span><span class="sxs-lookup"><span data-stu-id="64b6f-122">Condition</span></span></p></th>
<th><p><span data-ttu-id="64b6f-123">Acción</span><span class="sxs-lookup"><span data-stu-id="64b6f-123">Action</span></span></p></th>
<th><p><span data-ttu-id="64b6f-124">Argumentos</span><span class="sxs-lookup"><span data-stu-id="64b6f-124">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="64b6f-125"><strong>Definirvariabletemporal</strong></span><span class="sxs-lookup"><span data-stu-id="64b6f-125"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="64b6f-126"><strong>Name</strong>:<strong>expresión</strong>myVar: InputBox (&quot;especifique un número distinto de cero)&quot;.</span><span class="sxs-lookup"><span data-stu-id="64b6f-126"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64b6f-127">[TempVars]![MyVar]&lt;&gt;0</span><span class="sxs-lookup"><span data-stu-id="64b6f-127">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="64b6f-128"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="64b6f-128"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="64b6f-129"><strong>Mensaje</strong>: =&quot;ha escrito &quot; &amp; [TempVars]! MiVar &amp; &quot;. &quot; <strong>Bip</strong>: <strong>SíTipo</strong>: <strong>información</strong></span><span class="sxs-lookup"><span data-stu-id="64b6f-129"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="64b6f-130"><strong>QuitarVariableTemporal</strong></span><span class="sxs-lookup"><span data-stu-id="64b6f-130"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="64b6f-131"><strong>Nombre</strong>: MiVar</span><span class="sxs-lookup"><span data-stu-id="64b6f-131"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

