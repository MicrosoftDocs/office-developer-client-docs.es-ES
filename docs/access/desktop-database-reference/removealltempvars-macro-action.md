---
title: QuitarTodasLasVariablesTemporales (acción de macro)
TOCTitle: RemoveAllTempVars macro action
ms:assetid: 409fd836-4a53-cefd-4264-8cee0fa8ac52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192877(v=office.15)
ms:contentKeyID: 48544430
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117413
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c8ad54044bc457d5d513adb320c59b5a3d415215
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927413"
---
# <a name="removealltempvars-macro-action"></a><span data-ttu-id="03c6e-102">QuitarTodasLasVariablesTemporales (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="03c6e-102">RemoveAllTempVars macro action</span></span>


<span data-ttu-id="03c6e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="03c6e-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="03c6e-104">Puede usar la acción **QuitarTodasLasVariablesTemporales** para quitar todas las variables temporales creadas mediante la acción **DefinirVariableTemporal**.</span><span class="sxs-lookup"><span data-stu-id="03c6e-104">You can use the **RemoveAllTempVars** action to remove any temporary variables that you created by using the **SetTempVar** action.</span></span>

## <a name="setting"></a><span data-ttu-id="03c6e-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="03c6e-105">Setting</span></span>

<span data-ttu-id="03c6e-106">La acción **QuitarTodasLasVariablesTemporales** no tiene argumentos.</span><span class="sxs-lookup"><span data-stu-id="03c6e-106">The **RemoveAllTempVars** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="03c6e-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="03c6e-107">Remarks</span></span>

  - <span data-ttu-id="03c6e-p101">Puede haber hasta 255 variables temporales definidas a la vez. Si no se quita una variable temporal, se mantiene en la memoria hasta que se cierre la base de datos o el proyecto. Se recomienda quitar las variables temporales cuando termine de usarlas.</span><span class="sxs-lookup"><span data-stu-id="03c6e-p101">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database or project. It is a good practice to remove temporary variables when you are finished using them.</span></span>

  - <span data-ttu-id="03c6e-111">Access quita automáticamente todas las variables temporales cuando se cierra la base de datos o el proyecto.</span><span class="sxs-lookup"><span data-stu-id="03c6e-111">Access automatically removes all temporary variables when you close the database or project.</span></span>

  - <span data-ttu-id="03c6e-112">Para quitar una sola variable temporal, use la acción **QuitarVariableTemporal** y establezca su argumento en el nombre de la variable temporal que desee quitar.</span><span class="sxs-lookup"><span data-stu-id="03c6e-112">To remove a single temporary variable, use the **RemoveTempVar** action and set its argument to the name of the temporary variable you want to remove.</span></span>

  - <span data-ttu-id="03c6e-113">Para ejecutar la acción **QuitarTodasLasVariablesTemporales** en un módulo de VBA, use el método **RemoveAll** del objeto **TempVars**.</span><span class="sxs-lookup"><span data-stu-id="03c6e-113">To run the **RemoveAllTempVars** action in a VBA module, use the **RemoveAll** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="03c6e-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="03c6e-114">Example</span></span>

<span data-ttu-id="03c6e-115">En la siguiente macro se muestra cómo crear una variable temporal, cómo usarla en una condición y un cuadro de mensaje y, a continuación, cómo quitarla mediante la acción **QuitarTodasLasVariablesTemporales**.</span><span class="sxs-lookup"><span data-stu-id="03c6e-115">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveAllTempVars** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03c6e-116">Condición</span><span class="sxs-lookup"><span data-stu-id="03c6e-116">Condition</span></span></p></th>
<th><p><span data-ttu-id="03c6e-117">Acción</span><span class="sxs-lookup"><span data-stu-id="03c6e-117">Action</span></span></p></th>
<th><p><span data-ttu-id="03c6e-118">Argumentos</span><span class="sxs-lookup"><span data-stu-id="03c6e-118">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="03c6e-119"><strong>DefinirVariableTemporal</strong></span><span class="sxs-lookup"><span data-stu-id="03c6e-119"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="03c6e-120"><strong>Nombre</strong>: MiVar<strong>expresión</strong>: CuadroEntr (&quot;escriba un número distinto de cero.&quot;)</span><span class="sxs-lookup"><span data-stu-id="03c6e-120"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03c6e-121">[TempVars]![MyVar]&lt;&gt;0</span><span class="sxs-lookup"><span data-stu-id="03c6e-121">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="03c6e-122"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="03c6e-122"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="03c6e-123"><strong>Mensaje</strong>: =&quot;ha escrito &quot; &amp; [variables temporales]! [MiVar] &amp; &quot;. &quot; <strong>Bip</strong>: <strong>YesType</strong>: <strong>información</strong></span><span class="sxs-lookup"><span data-stu-id="03c6e-123"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="03c6e-124"><strong>QuitarTodasLasVariablesTemporales</strong></span><span class="sxs-lookup"><span data-stu-id="03c6e-124"><strong>RemoveAllTempVars</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

