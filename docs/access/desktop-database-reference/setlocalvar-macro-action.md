---
title: EstablecerVariableLocal (acción de macro)
TOCTitle: SetLocalVar macro action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 091b9717b9a2e35cfc8d0c8555e28570628065ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314591"
---
# <a name="setlocalvar-macro-action"></a><span data-ttu-id="73146-102">EstablecerVariableLocal (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="73146-102">SetLocalVar macro action</span></span>

<span data-ttu-id="73146-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="73146-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="73146-104">La acción **EstablecerVariableLocal** crea una variable temporal y la establece en un valor específico.</span><span class="sxs-lookup"><span data-stu-id="73146-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span>

## <a name="setting"></a><span data-ttu-id="73146-105">Valor</span><span class="sxs-lookup"><span data-stu-id="73146-105">Setting</span></span>

<span data-ttu-id="73146-106">La acción **EstablecerVariableLocal** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="73146-106">The **SetLocalVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73146-107">Argumento</span><span class="sxs-lookup"><span data-stu-id="73146-107">argument</span></span></p></th>
<th><p><span data-ttu-id="73146-108">Necesario</span><span class="sxs-lookup"><span data-stu-id="73146-108">Required</span></span></p></th>
<th><p><span data-ttu-id="73146-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="73146-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73146-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="73146-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="73146-111">Sí</span><span class="sxs-lookup"><span data-stu-id="73146-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="73146-112">Una cadena que especifica el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="73146-112">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73146-113"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="73146-113"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="73146-114">Sí</span><span class="sxs-lookup"><span data-stu-id="73146-114">Yes</span></span></p></td>
<td><p><span data-ttu-id="73146-115">Una expresión que se utilizará para establecer el valor de esta variable temporal.</span><span class="sxs-lookup"><span data-stu-id="73146-115">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="73146-116">No anteponga el signo igual (=) a la expresión.</span><span class="sxs-lookup"><span data-stu-id="73146-116">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="73146-117">Puede hacer clic en el botón <strong>Generar</strong> para utilizar el <strong>Generador de expresiones</strong> para establecer este argumento.</span><span class="sxs-lookup"><span data-stu-id="73146-117">You can click the <strong>Build</strong> button  to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="73146-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="73146-118">Remarks</span></span>

<span data-ttu-id="73146-p102">Las variables creadas por la acción **EstablecerVariableLocal** solo pueden utilizarse en la macro en la que se han definido. Utilice la acción **[DefinirVariableTemporal](settempvar-macro-action.md)** para definir una variable que puede utilizarse en otra macro, en un procedimiento de evento o en un formulario o informe.</span><span class="sxs-lookup"><span data-stu-id="73146-p102">Variables created by the **SetLocalVar** action can be used only in the macro in which they are defined. Use the **[SetTempVar](settempvar-macro-action.md)** action to define a variable that can be used in another macro, in an event procedure, or on a form or report.</span></span>

<span data-ttu-id="73146-p103">Una vez creada una variable temporal, puede hacer referencia a ella en una expresión. Por ejemplo, si ha creado una variable temporal denominada TotalAmount, puede utilizar la variable como el origen del control para un cuadro de texto mediante la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="73146-p103">Once a temporary variable has been created, you can refer to it in an expression. For example, if you created a temporary variable named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.</span></span>

`=[LocalVars]![TotalAmount]`

> [!NOTE]
> <span data-ttu-id="73146-123">En una Macro de datos, no tendrá que utilizar la colección de VariablesLocales para hacer referencia a una variable.</span><span class="sxs-lookup"><span data-stu-id="73146-123">In a Data Macro, you do not have to use the LocalVars collection to refer to a variable.</span></span> <span data-ttu-id="73146-124">Por ejemplo, si ha creado una variable temporal en una macro de datos denominada TotalAmount, puede utilizar la variable como el origen del control para un cuadro de texto mediante la sintaxis siguiente: `=[TotalAmount]`.</span><span class="sxs-lookup"><span data-stu-id="73146-124">For example, if you created a temporary variable in a Data Macro named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.</span></span>

