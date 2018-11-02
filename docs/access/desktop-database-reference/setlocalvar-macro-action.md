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
ms.openlocfilehash: b6db77a3cd712717e5aa2eb22e89f90557a1dabf
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926020"
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
<td><p><strong>Expresión</strong></p></td>
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
> <P>[!NOTA] En una macro de datos, no es necesario utilizar la colección LocalVars para hacer referencia a una variable. Por ejemplo, si ha creado una variable temporal en una Macro de datos denominado TotalAmount, se podría usar la variable como el origen del control para un cuadro de texto utilizando la sintaxis siguiente<BR>= [TotalAmount]</P>


