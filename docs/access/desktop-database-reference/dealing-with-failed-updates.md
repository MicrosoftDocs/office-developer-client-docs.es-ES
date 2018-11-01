---
title: Tratar actualizaciones con errores
TOCTitle: Dealing with Failed Updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca4d8d2fd8797ffb5ae0861e86dfa02faf7bb62c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875780"
---
# <a name="dealing-with-failed-updates"></a>Tratar actualizaciones con errores


**Se aplica a**: Access 2013, Office 2013

## <a name="dealing-with-failed-updates"></a>Tratamiento de las actualizaciones con errores

Cuando una actualización concluye con errores, la forma de resolver los errores depende de la naturaleza y la gravedad de los errores y de la lógica de la aplicación. Sin embargo, si la base de datos se comparte con otros usuarios, un error habitual es que otro usuario modifique el campo antes que usted. Este tipo de error se denomina *conflicto*. ADO detecta esta situación e informa de un error.

Si hay errores de actualización, se capturarán en una rutina de tratamiento de errores. Filtrar el **conjunto de registros** con la constante **adFilterConflictingRecords** para que sean visibles sólo las filas en conflicto. En este ejemplo, la estrategia de resolución de errores consiste simplemente en imprimir el autor del primer y el apellido (**au\_fname** y **au\_apellidos**).

El código para avisar al usuario del conflicto de actualización tiene este aspecto:

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

