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
# <a name="rundatamacro-macro-action"></a>EjecutarMacroDeDatos (acción de macro)

**Se aplica a**: Access 2013, Office 2013

Puede utilizar la acción **EjecutarMacroDeDatos** para ejecutar una macro de datos con nombre.

## <a name="setting"></a>Valores

La acción **EjecutarMacroDeDatos** tiene el siguiente argumento.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de la acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Nombre</p></td>
<td><p>Nombre de la macro de datos que se va a ejecutar.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Puede utilizar la acción **EjecutarMacroDeDatos** en macros, macros de datos con nombre y en los siguientes eventos de macro: **[Después de eliminar](after-delete-macro-event.md)**, **[Después de insertar](after-insert-macro-event.md)** y **[Después de actualizar](after-update-macro-event.md)**.

El nombre de la macro de datos debe incluir en la tabla a la que está conectado (por ejemplo, **Comments.AddComment**, no sólo **AddComment**).

Cuando selecciona la macro de datos que desea ejecutar en el Diseñador de macros, Access determina si la macro de datos requiere parámetros. Si la macro de datos requiere parámetros, se mostrarán cuadros de texto que se puede escribir en los argumentos.

Cuando se ejecuta una macro que contiene la acción **EjecutarMacroDeDatos** y se llega a la acción **EjecutarMacroDeDatos**, Access ejecuta la macro de datos a la que se ha llamado. Cuando esta macro de datos termina, Access vuelve a la macro original y ejecuta la acción siguiente.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo pasar un parámetro a una macro de datos con nombre. La macro de datos dmGetCurrentServiceRequest de la tabla tblServiceRequests se denomina mediante el uso de la acción EjecutarMacroDeDatos. Cuando finalice la dmGetCurrentServiceRequest, la variable CurrentServiceRequest devuelto por que la macro de datos se escribe en el cuadro de texto txtCurrentSR.

**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
