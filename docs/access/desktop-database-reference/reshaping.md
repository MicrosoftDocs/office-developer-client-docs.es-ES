---
title: Forma (referencia de escritorio de la base de datos de Access)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c820e82669789d7c3806cc1fd38a2eb6844b722e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711906"
---
# <a name="reshaping"></a><span data-ttu-id="72fa1-102">Cambio de forma</span><span class="sxs-lookup"><span data-stu-id="72fa1-102">Reshaping</span></span>

<span data-ttu-id="72fa1-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="72fa1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="72fa1-p101">A un objeto **Recordset** creado mediante una cláusula de un comando Shape se le puede asignar un nombre de *alias* (normalmente con la palabra clave AS). Se puede usar un comando totalmente diferente para hacer referencia al alias de un objeto **Recordset** con forma. Es decir, se puede volver a utilizar, o *crear con nuevas formas*, un objeto **Recordset** al que se aplicó forma anteriormente, en un nuevo comando Shape. Para admitir esta característica, ADO proporciona una propiedad [Reshape Name](reshape-name-property-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="72fa1-p101">A **Recordset** created by a clause of a shape command may be assigned an *alias* name (typically with the AS keyword). The alias of a shaped **Recordset** can be referenced in an entirely different command. That is, you may reuse, or *reshape*, a previously shaped **Recordset** in a new shape command. To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).</span></span>

<span data-ttu-id="72fa1-p102">Las nuevas formas cumplen dos funciones principales. La primera es asociar un objeto **Recordset** existente a un nuevo objeto **Recordset** principal.</span><span class="sxs-lookup"><span data-stu-id="72fa1-p102">Reshaping has two main functions. The first is to associate an existing **Recordset** with a new parent **Recordset**.</span></span>

## <a name="example"></a><span data-ttu-id="72fa1-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="72fa1-110">Example</span></span>

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

<span data-ttu-id="72fa1-111">La segunda función consiste en habilitar el acceso no estructurado en capítulos en los objetos **Recordset** secundarios existentes, mediante la sintaxis `"SHAPE <recordset reshape name>"`.</span><span class="sxs-lookup"><span data-stu-id="72fa1-111">The second function is to enable non-chaptered access to existing child **Recordset** objects, using the syntax `"SHAPE <recordset reshape name>"`.</span></span>

> [!NOTE]
> <span data-ttu-id="72fa1-112">[!NOTA] No se pueden anexar columnas a un objeto **Recordset** existente, crear nuevas formas para un objeto **Recordset** parametrizado o los objetos **Recordset** de cualquier cláusula COMPUTE intermedia, ni realizar operaciones de agregado en cualquier objeto **Recordset** descendiente del objeto **Recordset** que se está creando con nuevas formas.</span><span class="sxs-lookup"><span data-stu-id="72fa1-112">You cannot append columns to an existing **Recordset**, reshape a parameterized **Recordset** or the **Recordset** objects in any intervening COMPUTE clause, or perform aggregate operations on any **Recordset** descendant from the **Recordset** being reshaped.</span></span> <span data-ttu-id="72fa1-113">El **conjunto de registros** que se va a cambiar la forma y la nueva forma de comando deben utilizar ambos el mismo \*\* objeto[Connection](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="72fa1-113">The **Recordset** being reshaped and the new shape command must both use the same \*\*[Connection](connection-object-ado.md) object.</span></span>


