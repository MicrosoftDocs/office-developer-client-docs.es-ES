---
title: EstablecerVariableLocal (acción de macro)
TOCTitle: SetLocalVar macro action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 091b9717b9a2e35cfc8d0c8555e28570628065ef
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702463"
---
# <a name="setlocalvar-macro-action"></a>EstablecerVariableLocal (acción de macro)

**Se aplica a**: Access 2013, Office 2013

La acción **EstablecerVariableLocal** crea una variable temporal y la establece en un valor específico.

## <a name="setting"></a>Valores

La acción **EstablecerVariableLocal** utiliza los siguientes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Obligatorio</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Name</strong></p></td>
<td><p>Sí</p></td>
<td><p>Una cadena que especifica el nombre de la variable.</p></td>
</tr>
<tr class="even">
<td><p><strong>Expression</strong></p></td>
<td><p>Sí</p></td>
<td><p>Una expresión que se usará para establecer el valor de esta variable temporal. Delante de la expresión con el signo igual (=). Puede hacer clic en el botón <strong>Generar</strong> para usar el <strong>Generador de expresiones</strong> para definir este argumento.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Comentarios

Las variables creadas por la acción **EstablecerVariableLocal** solo pueden utilizarse en la macro en la que se han definido. Utilice la acción **[DefinirVariableTemporal](settempvar-macro-action.md)** para definir una variable que puede utilizarse en otra macro, en un procedimiento de evento o en un formulario o informe.

Una vez creada una variable temporal, puede hacer referencia a ella en una expresión. Por ejemplo, si ha creado una variable temporal denominada TotalAmount, puede utilizar la variable como el origen del control para un cuadro de texto mediante la sintaxis siguiente.

`=[LocalVars]![TotalAmount]`

> [!NOTE]
> [!NOTA] En una macro de datos, no es necesario utilizar la colección LocalVars para hacer referencia a una variable. Por ejemplo, si ha creado una variable temporal en una Macro de datos denominado TotalAmount, se podría usar la variable como el origen del control para un cuadro de texto utilizando la sintaxis siguiente: `=[TotalAmount]`.

