---
title: EjecutarMacroDeDatos (acción de macro)
TOCTitle: RunDataMacro Macro Action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6777ae05d2ab7455016df834d17abb3406a2d710
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889927"
---
# <a name="rundatamacro-macro-action"></a><span data-ttu-id="9b5c5-102">EjecutarMacroDeDatos (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="9b5c5-102">RunDataMacro Macro Action</span></span>

<span data-ttu-id="9b5c5-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b5c5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b5c5-104">Puede utilizar la acción **EjecutarMacroDeDatos** para ejecutar una macro de datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="9b5c5-104">You can use the **RunDataMacro** action to run a named data macro.</span></span>

## <a name="setting"></a><span data-ttu-id="9b5c5-105">Valores</span><span class="sxs-lookup"><span data-stu-id="9b5c5-105">Setting</span></span>

<span data-ttu-id="9b5c5-106">La acción **EjecutarMacroDeDatos** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="9b5c5-106">The **RunDataMacro** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b5c5-107">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="9b5c5-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="9b5c5-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b5c5-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b5c5-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="9b5c5-109">Name</span></span></p></td>
<td><p><span data-ttu-id="9b5c5-110">Nombre de la macro de datos que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="9b5c5-110">The name of the data macro to run.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9b5c5-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9b5c5-111">Remarks</span></span>

<span data-ttu-id="9b5c5-112">Puede utilizar la acción **EjecutarMacroDeDatos** en macros, macros de datos con nombre y en los siguientes eventos de macro: **[Después de eliminar](after-delete-macro-event.md)**, **[Después de insertar](after-insert-macro-event.md)** y **[Después de actualizar](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="9b5c5-112">You can use the **RunDataMacro** action in macros, named data macros, and the following macro events: **[After Delete Macro Event](after-delete-macro-event.md)**, **[After Insert Macro Event](after-insert-macro-event.md)** and **[After Update Macro Event](after-update-macro-event.md)**.</span></span>

<span data-ttu-id="9b5c5-113">El nombre de la macro de datos debe incluir en la tabla a la que está conectado (por ejemplo, **Comments.AddComment**, no sólo **AddComment**).</span><span class="sxs-lookup"><span data-stu-id="9b5c5-113">The name of the data macro must include the table to which it is attached (for example, **Comments.AddComment**, not just **AddComment**).</span></span>

<span data-ttu-id="9b5c5-114">Cuando selecciona la macro de datos que desea ejecutar en el Diseñador de macros, Access determina si la macro de datos requiere parámetros.</span><span class="sxs-lookup"><span data-stu-id="9b5c5-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="9b5c5-115">Si la macro de datos requiere parámetros, se mostrarán cuadros de texto que se puede escribir en los argumentos.</span><span class="sxs-lookup"><span data-stu-id="9b5c5-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>

<span data-ttu-id="9b5c5-p102">Cuando se ejecuta una macro que contiene la acción **EjecutarMacroDeDatos** y se llega a la acción **EjecutarMacroDeDatos**, Access ejecuta la macro de datos a la que se ha llamado. Cuando esta macro de datos termina, Access vuelve a la macro original y ejecuta la acción siguiente.</span><span class="sxs-lookup"><span data-stu-id="9b5c5-p102">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span>

## <a name="example"></a><span data-ttu-id="9b5c5-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b5c5-118">Example</span></span>

<span data-ttu-id="9b5c5-119">En el ejemplo siguiente se muestra cómo pasar un parámetro a una macro de datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="9b5c5-119">The following example shows how to pass a parameter to a named data macro.</span></span> <span data-ttu-id="9b5c5-120">La macro de datos dmGetCurrentServiceRequest de la tabla tblServiceRequests se denomina mediante el uso de la acción EjecutarMacroDeDatos.</span><span class="sxs-lookup"><span data-stu-id="9b5c5-120">The dmGetCurrentServiceRequest data macro of the tblServiceRequests table is called by using the RunDataMacro action.</span></span> <span data-ttu-id="9b5c5-121">Cuando finalice la dmGetCurrentServiceRequest, la variable CurrentServiceRequest devuelto por que la macro de datos se escribe en el cuadro de texto txtCurrentSR.</span><span class="sxs-lookup"><span data-stu-id="9b5c5-121">When the dmGetCurrentServiceRequest is finished, the CurrentServiceRequest variable returned form the data macro is written to the txtCurrentSR text box.</span></span>

<span data-ttu-id="9b5c5-122">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="9b5c5-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```
