---
title: EstablecerVariableLocal (acción de macro)
TOCTitle: SetLocalVar Macro Action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fb2b3aabb4736c0deee57dafb36e32730fb95f4f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486827"
---
# <a name="setlocalvar-macro-action"></a><span data-ttu-id="4c11c-102">EstablecerVariableLocal (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="4c11c-102">SetLocalVar Macro Action</span></span>


<span data-ttu-id="4c11c-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c11c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4c11c-104">La acción **EstablecerVariableLocal** crea una variable temporal y la establece en un valor específico.</span><span class="sxs-lookup"><span data-stu-id="4c11c-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span>

## <a name="setting"></a><span data-ttu-id="4c11c-105">Valores</span><span class="sxs-lookup"><span data-stu-id="4c11c-105">Setting</span></span>

<span data-ttu-id="4c11c-106">La acción **EstablecerVariableLocal** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="4c11c-106">The **SetLocalVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4c11c-107">Argumento</span><span class="sxs-lookup"><span data-stu-id="4c11c-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="4c11c-108">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4c11c-108">Required</span></span></p></th>
<th><p><span data-ttu-id="4c11c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c11c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c11c-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="4c11c-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="4c11c-111">Sí</span><span class="sxs-lookup"><span data-stu-id="4c11c-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="4c11c-112">Una cadena que especifica el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="4c11c-112">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c11c-113"><strong>Expresión</strong></span><span class="sxs-lookup"><span data-stu-id="4c11c-113"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="4c11c-114">Sí</span><span class="sxs-lookup"><span data-stu-id="4c11c-114">Yes</span></span></p></td>
<td><p><span data-ttu-id="4c11c-115">Una expresión que se usará para establecer el valor de esta variable temporal.</span><span class="sxs-lookup"><span data-stu-id="4c11c-115">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="4c11c-116">Delante de la expresión con el signo igual (=).</span><span class="sxs-lookup"><span data-stu-id="4c11c-116">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="4c11c-117">Puede hacer clic en el botón <strong>Generar</strong> para usar el <strong>Generador de expresiones</strong> para definir este argumento.</span><span class="sxs-lookup"><span data-stu-id="4c11c-117">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4c11c-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4c11c-118">Remarks</span></span>

<span data-ttu-id="4c11c-p102">Las variables creadas por la acción **EstablecerVariableLocal** solo pueden utilizarse en la macro en la que se han definido. Utilice la acción **[DefinirVariableTemporal](settempvar-macro-action.md)** para definir una variable que puede utilizarse en otra macro, en un procedimiento de evento o en un formulario o informe.</span><span class="sxs-lookup"><span data-stu-id="4c11c-p102">Variables created by the **SetLocalVar** action can be used only in the macro in which they are defined. Use the **[SetTempVar](settempvar-macro-action.md)** action to define a variable that can be used in another macro, in an event procedure, or on a form or report.</span></span>

<span data-ttu-id="4c11c-p103">Una vez creada una variable temporal, puede hacer referencia a ella en una expresión. Por ejemplo, si ha creado una variable temporal denominada TotalAmount, puede utilizar la variable como el origen del control para un cuadro de texto mediante la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="4c11c-p103">Once a temporary variable has been created, you can refer to it in an expression. For example, if you created a temporary variable named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.</span></span>

`=[LocalVars]![TotalAmount]`


> [!NOTE]
> <P><span data-ttu-id="4c11c-123">[!NOTA] En una macro de datos, no es necesario utilizar la colección LocalVars para hacer referencia a una variable.</span><span class="sxs-lookup"><span data-stu-id="4c11c-123">In a Data Macro, you do not have to use the LocalVars collection to refer to a variable.</span></span> <span data-ttu-id="4c11c-124">Por ejemplo, si ha creado una variable temporal en una Macro de datos denominado TotalAmount, se podría usar la variable como el origen del control para un cuadro de texto utilizando la sintaxis siguiente</span><span class="sxs-lookup"><span data-stu-id="4c11c-124">For example, if you created a temporary variable in a Data Macro named TotalAmount, you could use the variable as the control source for a text box by using the following syntax</span></span><BR><span data-ttu-id="4c11c-125">= [TotalAmount]</span><span class="sxs-lookup"><span data-stu-id="4c11c-125">=[TotalAmount]</span></span></P>


