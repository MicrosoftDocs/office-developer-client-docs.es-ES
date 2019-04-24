---
title: EjecutarMacroDeDatos (acción de macro)
TOCTitle: RunDataMacro macro action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 32945f0822682a9432d75ed1ac59117dde3cc0e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306814"
---
# <a name="rundatamacro-macro-action"></a>EjecutarMacroDeDatos (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede utilizar la acción **EjecutarMacroDeDatos** para ejecutar una macro de datos con nombre.

## <a name="setting"></a>Configuración

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
<td><p>Name</p></td>
<td><p>Nombre de la macro de datos que se va a ejecutar.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Puede usar la acción **RunDataMacro** en macros, macros de datos con nombre y los siguientes eventos de macro: **[después de eliminar](after-delete-macro-event.md)** el evento de macro, después de insertar evento de **[macro](after-insert-macro-event.md)** y **[después de actualizar evento de macro](after-update-macro-event.md)**.

El nombre de la macro de datos debe incluir la tabla a la que está asociada (por ejemplo, **comments. AddComment**, no solo **AddComment**).

Cuando selecciona la macro de datos que desea ejecutar en el Diseñador de macros, Access determina si la macro de datos requiere parámetros. Si la macro de datos requiere parámetros, aparecerán cuadros de texto en los que puede escribir los argumentos.

Cuando se ejecuta una macro que contiene la acción **EjecutarMacroDeDatos** y se llega a la acción **EjecutarMacroDeDatos**, Access ejecuta la macro de datos a la que se ha llamado. Cuando esta macro de datos termina, Access vuelve a la macro original y ejecuta la acción siguiente.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo pasar un parámetro a una macro de datos con nombre. Se llama a la macro de datos dmGetCurrentServiceRequest de la tabla tblServiceRequests mediante la acción RunDataMacro. Una vez finalizada la dmGetCurrentServiceRequest, la variable CurrentServiceRequest devuelta el formulario la macro de datos se escribe en el cuadro de texto txtCurrentSR.

**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
