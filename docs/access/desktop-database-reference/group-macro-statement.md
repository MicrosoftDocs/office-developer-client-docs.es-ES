---
title: Grupo (instrucción de macro)
TOCTitle: Group Macro Statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 189744d228db0dadd3260ce77457daf8724828f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484818"
---
# <a name="group-macro-statement"></a>Grupo (instrucción de macro)


**Se aplica a**: Access 2013 | Office 2013

La instrucción **grupo** permite especificar un bloque de acciones dentro de una macro que se puede expandir o contraer.

## <a name="setting"></a>Valores

La acción **Grupo** utiliza los siguientes argumentos.

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
<td><p><strong>Descripción</strong></p></td>
<td><p>No</p></td>
<td><p>Una cadena que aparece como el título de un grupo cuando está contraída.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

La instrucción **Grupo** no define una región de una macro que se puede ejecutar por separado. Utilice la instrucción **[Submacro](submacro-macro-statement.md)** para definir un conjunto de acciones que se va a ejecutar por separado en la ventana **Diseñador de macros**.

