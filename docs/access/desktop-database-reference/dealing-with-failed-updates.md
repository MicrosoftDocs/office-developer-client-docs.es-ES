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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294165"
---
# <a name="dealing-with-failed-updates"></a>Tratamiento de las actualizaciones con errores

**Se aplica a:** Access 2013, Office 2013

## <a name="dealing-with-failed-updates"></a>Tratar actualizaciones con errores

Cuando una actualización concluye con errores, la forma de resolver los errores depende de la naturaleza y la gravedad de los errores y de la lógica de la aplicación. Sin embargo, si la base de datos se comparte con otros usuarios, un error habitual es que otro usuario modifique el campo antes que usted. Este tipo de error se denomina *conflicto*. ADO detecta esta situación e informa de un error.

If there are update errors, they will be trapped in an error-handling routine. Filter the **Recordset** with the **adFilterConflictingRecords** constant so that only the conflicting rows are visible. En este ejemplo, la estrategia de resolución de errores es simplemente imprimir el nombre y los apellidos del autor (**au \_ fname** y **au \_ lname**).

El código para avisar al usuario del conflicto de actualización tiene este aspecto:

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

