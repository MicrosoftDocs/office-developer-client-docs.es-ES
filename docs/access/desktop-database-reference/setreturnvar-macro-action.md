---
title: EstablecerVariableDevuelta (acción de macro)
TOCTitle: SetReturnVar macro action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f73ba90b4eae9f5da17e27d466044d97fb815d74
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923794"
---
# <a name="setreturnvar-macro-action"></a><span data-ttu-id="e419d-102">EstablecerVariableDevuelta (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="e419d-102">SetReturnVar macro action</span></span>

<span data-ttu-id="e419d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e419d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e419d-104">La acción **SetReturnVar** crea una variable de retorno y establece en un valor específico.</span><span class="sxs-lookup"><span data-stu-id="e419d-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span>

> [!NOTE]
> <span data-ttu-id="e419d-105">La acción **SetReturnVar** sólo está disponible en Macros de datos.</span><span class="sxs-lookup"><span data-stu-id="e419d-105">The **SetReturnVar** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="e419d-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="e419d-106">Setting</span></span>

<span data-ttu-id="e419d-107">La acción **SetReturnVar** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="e419d-107">The **SetReturnVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e419d-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="e419d-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="e419d-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e419d-109">Required</span></span></p></th>
<th><p><span data-ttu-id="e419d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e419d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e419d-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="e419d-111">Name</span></span></p></td>
<td><p><span data-ttu-id="e419d-112">Sí</span><span class="sxs-lookup"><span data-stu-id="e419d-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="e419d-113">Una cadena que especifica el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="e419d-113">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e419d-114">Expresión</span><span class="sxs-lookup"><span data-stu-id="e419d-114">Expression</span></span></p></td>
<td><p><span data-ttu-id="e419d-115">Sí</span><span class="sxs-lookup"><span data-stu-id="e419d-115">Yes</span></span></p></td>
<td><p><span data-ttu-id="e419d-116">Una expresión que se usará para establecer el valor de esta variable temporal.</span><span class="sxs-lookup"><span data-stu-id="e419d-116">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="e419d-117">Delante de la expresión con el signo igual (=).</span><span class="sxs-lookup"><span data-stu-id="e419d-117">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="e419d-118">Puede hacer clic en el botón <strong>Generar</strong> para usar el <strong>Generador de expresiones</strong> para definir este argumento.</span><span class="sxs-lookup"><span data-stu-id="e419d-118">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e419d-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e419d-119">Remarks</span></span>

<span data-ttu-id="e419d-120">La acción **SetReturnVar** se usa para crear un **ReturnVar**, que es la variable que se puede utilizar las macros que llaman a una macro de datos mediante el uso de la acción **EjecutarMacroDeDatos** .</span><span class="sxs-lookup"><span data-stu-id="e419d-120">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span>

<span data-ttu-id="e419d-121">Una vez creada una **ReturnVar** por la acción **SetReturnVar** , la macro llamada puede usar en una expresión.</span><span class="sxs-lookup"><span data-stu-id="e419d-121">Once a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="e419d-122">Por ejemplo, si ha creado un **ReturnVar** denominado **UpdateSuccess**, podría usar la variable utilizando la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="e419d-122">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>

```vb
    =[ReturnVars]![UpdateSuccess]
```

<span data-ttu-id="e419d-123">La acción **SetReturnVar** se puede usar en macros de datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="e419d-123">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="e419d-124">No está disponible en macros de datos que están asociadas a un evento de macro de datos.</span><span class="sxs-lookup"><span data-stu-id="e419d-124">It is not available in data macros that are attached to a data macro event.</span></span>

## <a name="example"></a><span data-ttu-id="e419d-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e419d-125">Example</span></span>

<span data-ttu-id="e419d-126">En el ejemplo siguiente se muestra cómo usar la acción SetReturnVar para devolver un valor desde una macro de datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="e419d-126">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="e419d-127">Un ReturnVar denominado **CurrentServiceRequest** se devuelve a la macro o Visual Basic para la subrutina de aplicaciones (VBA) que llama a la macro de datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="e419d-127">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="e419d-128">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="e419d-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
