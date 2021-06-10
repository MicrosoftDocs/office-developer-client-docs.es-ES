---
title: DefinirVariableTemporal (acción de macro)
TOCTitle: SetTempVar macro action
ms:assetid: 9c3b7bee-02c5-efbf-1276-4c4a1f7802d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198102(v=office.15)
ms:contentKeyID: 48546593
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm150219
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b630304774e521162687d4c78a6a97cf18ddb419
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306527"
---
# <a name="settempvar-macro-action"></a><span data-ttu-id="59c03-102">DefinirVariableTemporal (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="59c03-102">SetTempVar macro action</span></span>


<span data-ttu-id="59c03-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="59c03-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="59c03-p101">Puede usar la acción **DefinirVariableTemporal** para crear una variable temporal y establecerla en un valor específico. A continuación, podrá usar la variable como condición o argumento en acciones subsiguientes, o bien, usarla en otra macro, un procedimiento de evento o en un formulario o informe.</span><span class="sxs-lookup"><span data-stu-id="59c03-p101">You can use the **SetTempVar** action to create a temporary variable and set it to a specific value. The variable can then be used as a condition or argument in subsequent actions, or you can use the variable in another macro, in an event procedure, or on a form or report.</span></span>

## <a name="setting"></a><span data-ttu-id="59c03-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="59c03-106">Setting</span></span>

<span data-ttu-id="59c03-107">La acción **DefinirVariableTemporal** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="59c03-107">The **SetTempVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="59c03-108">Argumento de acción</span><span class="sxs-lookup"><span data-stu-id="59c03-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="59c03-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="59c03-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59c03-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="59c03-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="59c03-111">Especifique el nombre de la variable temporal.</span><span class="sxs-lookup"><span data-stu-id="59c03-111">Enter the name of the temporary variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c03-112"><strong>Expresión</strong></span><span class="sxs-lookup"><span data-stu-id="59c03-112"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="59c03-113">Escriba una expresión que se usará para establecer el valor de esta variable temporal.</span><span class="sxs-lookup"><span data-stu-id="59c03-113">Enter an expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="59c03-114">No anteponga la expresión con el signo igual ( <strong>=</strong> ) .</span><span class="sxs-lookup"><span data-stu-id="59c03-114">Do not precede the expression with the equal (<strong>=</strong>) sign.</span></span> <span data-ttu-id="59c03-115">Puede hacer clic en el <strong>botón Generar</strong></span><span class="sxs-lookup"><span data-stu-id="59c03-115">You can click the <strong>Build</strong> button</span></span> <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> <span data-ttu-id="59c03-117">para usar el Generador de expresiones para establecer este argumento.</span><span class="sxs-lookup"><span data-stu-id="59c03-117">to use the Expression Builder to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="59c03-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="59c03-118">Remarks</span></span>

- <span data-ttu-id="59c03-p103">Puede haber hasta 255 variables temporales definidas a la vez. Si no quita una variable temporal, esta permanecerá en la memoria hasta que se cierre la base de datos. Se recomienda quitar las variables temporales cuando termine de usarlas. Para quitar una sola variable temporal, use la acción **[QuitarVariableTemporal](removetempvar-macro-action.md)** y establezca su argumento en el nombre de la variable temporal que quiera quitar. Si hay más de una variable temporal y quiere quitarlas todas a la vez, use la acción **QuitarTodasLasVariablesTemporales**.</span><span class="sxs-lookup"><span data-stu-id="59c03-p103">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database. It is a good practice to remove temporary variables when you are finished using them. To remove a single temporary variable, use the **[RemoveTempVar](removetempvar-macro-action.md)** action and set its argument to the name of the temporary variable that you want to remove. If you have more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

- <span data-ttu-id="59c03-124">Las variables temporales son globales.</span><span class="sxs-lookup"><span data-stu-id="59c03-124">Temporary variables are global.</span></span> <span data-ttu-id="59c03-125">Una vez creada una variable temporal, podrá referirse a la misma en un procedimiento de evento, un módulo de Visual Basic para Aplicaciones (VBA), una consulta o una expresión.</span><span class="sxs-lookup"><span data-stu-id="59c03-125">Once a temporary variable has been created, you can refer to it in an event procedure, a Visual Basic for Applications (VBA) module, a query, or an expression.</span></span> <span data-ttu-id="59c03-126">Por ejemplo, si creó una variable temporal denominada *MyVar*, podría usar la variable como origen de control para un cuadro de texto mediante la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="59c03-126">For example, if you created a temporary variable named *MyVar*, you could use the variable as the control source for a text box by using the following syntax:</span></span>
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > <span data-ttu-id="59c03-127">En las macros, las consultas y los procedimientos de eventos, la expresión no debe ir precedida de un signo de igualdad.</span><span class="sxs-lookup"><span data-stu-id="59c03-127">In macros, queries and event procedures, you do not need to precede the expression with an equal sign.</span></span>
 
  <span data-ttu-id="59c03-128">Asimismo, puede referirse a las variables temporales en complementos o bases de datos de referencia.</span><span class="sxs-lookup"><span data-stu-id="59c03-128">You can also refer to temporary variables in any add-ins or referenced databases.</span></span>

- <span data-ttu-id="59c03-129">Para ejecutar la acción **DefinirVariableTemporal** en un módulo de VBA, use el método **Add** del objeto **TempVars**.</span><span class="sxs-lookup"><span data-stu-id="59c03-129">To run the **SetTempVar** action in a VBA module, use the **Add** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="59c03-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="59c03-130">Example</span></span>

<span data-ttu-id="59c03-131">En la siguiente macro se muestra cómo crear una variable temporal mediante la acción **DefinirVariableTemporal**, cómo se usa la variable temporal en una condición y un cuadro de mensaje y cómo se quita la variable temporal.</span><span class="sxs-lookup"><span data-stu-id="59c03-131">The following macro demonstrates how to create a temporary variable by using the **SetTempVar** action, then using the temporary variable in a condition and a message box, and then removing the temporary variable.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="59c03-132">Condición</span><span class="sxs-lookup"><span data-stu-id="59c03-132">Condition</span></span></p></th>
<th><p><span data-ttu-id="59c03-133">Acción</span><span class="sxs-lookup"><span data-stu-id="59c03-133">Action</span></span></p></th>
<th><p><span data-ttu-id="59c03-134">Argumentos</span><span class="sxs-lookup"><span data-stu-id="59c03-134">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="59c03-135"><strong>SetTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="59c03-135"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="59c03-136"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox( &quot; Enter a non-zero number. &quot; )</span><span class="sxs-lookup"><span data-stu-id="59c03-136"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c03-137">[TempVars]![MyVar]&lt;&gt;0</span><span class="sxs-lookup"><span data-stu-id="59c03-137">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="59c03-138"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="59c03-138"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="59c03-139"><strong>Message</strong>: = &quot; You entered &quot; &amp; [TempVars]![ MyVar] &amp; &quot; . &quot; <strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span><span class="sxs-lookup"><span data-stu-id="59c03-139"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="59c03-140"><strong>RemoveTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="59c03-140"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="59c03-141"><strong>Nombre</strong>: MiVar</span><span class="sxs-lookup"><span data-stu-id="59c03-141"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

