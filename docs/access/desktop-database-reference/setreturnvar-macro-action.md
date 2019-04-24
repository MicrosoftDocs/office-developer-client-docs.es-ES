---
title: EstablecerVariableDevuelta (acción de macro)
TOCTitle: SetReturnVar macro action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e0c849fc507d535807bc088e667acd74410ddd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308676"
---
# <a name="setreturnvar-macro-action"></a><span data-ttu-id="89b61-102">EstablecerVariableDevuelta (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="89b61-102">SetReturnVar macro action</span></span>

<span data-ttu-id="89b61-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89b61-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89b61-104">La acción **SetReturnVar** crea una variable de retorno y la establece en un valor específico.</span><span class="sxs-lookup"><span data-stu-id="89b61-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span>

> [!NOTE]
> <span data-ttu-id="89b61-105">La acción **SetReturnVar** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="89b61-105">The **SetReturnVar** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="89b61-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="89b61-106">Setting</span></span>

<span data-ttu-id="89b61-107">La acción **SetReturnVar** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="89b61-107">The **SetReturnVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89b61-108">Argument</span><span class="sxs-lookup"><span data-stu-id="89b61-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="89b61-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="89b61-109">Required</span></span></p></th>
<th><p><span data-ttu-id="89b61-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="89b61-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89b61-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="89b61-111">Name</span></span></p></td>
<td><p><span data-ttu-id="89b61-112">Sí</span><span class="sxs-lookup"><span data-stu-id="89b61-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="89b61-113">Una cadena que especifica el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="89b61-113">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89b61-114">Numérico</span><span class="sxs-lookup"><span data-stu-id="89b61-114">Expression</span></span></p></td>
<td><p><span data-ttu-id="89b61-115">Sí</span><span class="sxs-lookup"><span data-stu-id="89b61-115">Yes</span></span></p></td>
<td><p><span data-ttu-id="89b61-116">Una expresión que se utilizará para establecer el valor de esta variable temporal.</span><span class="sxs-lookup"><span data-stu-id="89b61-116">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="89b61-117">No anteponga el signo igual (=) a la expresión.</span><span class="sxs-lookup"><span data-stu-id="89b61-117">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="89b61-118">Puede hacer clic en el botón <strong>generar</strong> para usar el <strong>generador de expresiones</strong> para establecer este argumento.</span><span class="sxs-lookup"><span data-stu-id="89b61-118">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="89b61-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="89b61-119">Remarks</span></span>

<span data-ttu-id="89b61-120">La acción **SetReturnVar** se usa para crear una **ReturnVar**, que es una variable que pueden usar las macros que llaman a una macro de datos mediante la acción **RunDataMacro** .</span><span class="sxs-lookup"><span data-stu-id="89b61-120">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span>

<span data-ttu-id="89b61-121">Una vez que la acción **SetReturnVar** crea **ReturnVar** , la macro de llamada puede usarla en una expresión.</span><span class="sxs-lookup"><span data-stu-id="89b61-121">Once a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="89b61-122">Por ejemplo, si ha creado un **ReturnVar** con el nombre **UpdateSuccess**, puede usar la variable mediante la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="89b61-122">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>

```vb
    =[ReturnVars]![UpdateSuccess]
```

<span data-ttu-id="89b61-123">La acción **SetReturnVar** sólo se puede usar en macros de datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="89b61-123">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="89b61-124">No está disponible en macros de datos que estén adjuntas a un evento de macro de datos.</span><span class="sxs-lookup"><span data-stu-id="89b61-124">It is not available in data macros that are attached to a data macro event.</span></span>

## <a name="example"></a><span data-ttu-id="89b61-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="89b61-125">Example</span></span>

<span data-ttu-id="89b61-126">En el ejemplo siguiente se muestra cómo usar la acción SetReturnVar para devolver un valor de una macro de datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="89b61-126">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="89b61-127">Un ReturnVar denominado **CurrentServiceRequest** se devuelve a la subrutina o a la subrutina de Visual Basic para aplicaciones (VBA) que llama a la macro de datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="89b61-127">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="89b61-128">**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="89b61-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
