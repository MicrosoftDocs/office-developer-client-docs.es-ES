---
title: Tratamiento de las actualizaciones con errores
TOCTitle: Dealing with failed updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9a44548fd8747428b12c03c24207f36d3871e349
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725941"
---
# <a name="dealing-with-failed-updates"></a><span data-ttu-id="140e5-102">Tratamiento de las actualizaciones con errores</span><span class="sxs-lookup"><span data-stu-id="140e5-102">Dealing with failed updates</span></span>

<span data-ttu-id="140e5-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="140e5-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="dealing-with-failed-updates"></a><span data-ttu-id="140e5-104">Tratamiento de las actualizaciones con errores</span><span class="sxs-lookup"><span data-stu-id="140e5-104">Dealing with Failed Updates</span></span>

<span data-ttu-id="140e5-p101">Cuando una actualización concluye con errores, la forma de resolver los errores depende de la naturaleza y la gravedad de los errores y de la lógica de la aplicación. Sin embargo, si la base de datos se comparte con otros usuarios, un error habitual es que otro usuario modifique el campo antes que usted. Este tipo de error se denomina *conflicto*. ADO detecta esta situación e informa de un error.</span><span class="sxs-lookup"><span data-stu-id="140e5-p101">When an update concludes with errors, how you resolve the errors depends on the nature and severity of the errors and the logic of your application. However, if the database is shared with other users, a typical error is that someone else modifies the field before you do. This type of error is called a *conflict.* ADO detects this situation and reports an error.</span></span>

<span data-ttu-id="140e5-109">Si hay errores de actualización, se capturarán en una rutina de tratamiento de errores.</span><span class="sxs-lookup"><span data-stu-id="140e5-109">If there are update errors, they will be trapped in an error-handling routine.</span></span> <span data-ttu-id="140e5-110">Filtrar el **conjunto de registros** con la constante **adFilterConflictingRecords** para que sean visibles sólo las filas en conflicto.</span><span class="sxs-lookup"><span data-stu-id="140e5-110">Filter the **Recordset** with the **adFilterConflictingRecords** constant so that only the conflicting rows are visible.</span></span> <span data-ttu-id="140e5-111">En este ejemplo, la estrategia de resolución de errores consiste simplemente en imprimir el autor del primer y el apellido (**au\_fname** y **au\_apellidos**).</span><span class="sxs-lookup"><span data-stu-id="140e5-111">In this example, the error-resolution strategy is merely to print the author's first and last names (**au\_fname** and **au\_lname**).</span></span>

<span data-ttu-id="140e5-112">El código para avisar al usuario del conflicto de actualización tiene este aspecto:</span><span class="sxs-lookup"><span data-stu-id="140e5-112">The code to alert the user to the update conflict looks like this:</span></span>

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

