---
title: Grupo (instrucción de macro)
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2dc25621a49d8fd23078a926d6ec6c5de54e54d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292114"
---
# <a name="group-macro-statement"></a>Grupo (instrucción de macro)


**Se aplica a:** Access 2013, Office 2013

La **instrucción Group** permite especificar un bloque de acciones dentro de una macro que puede expandir o contraer.

## <a name="setting"></a>Setting

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
<th><p>Necesario</p></th>
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

