---
title: Workspace.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d062adbde4e9d7053e61342b7433939d4fbffcb8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483983"
---
# <a name="workspacetype-property-dao"></a>Workspace.Type Property (DAO)


**Se aplica a**: Access 2013 | Office 2013

Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto. **Integer** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Tipo de

*expresión* Variable que representa un objeto **Workspace** .

## <a name="remarks"></a>Observaciones

Para un objeto **Workspace**, los posibles valores de configuración y devueltos son los siguientes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Tipo de área de trabajo</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbUseJet</strong></p></td>
<td><p>El objeto <strong>Workspace</strong> está conectado al motor de base de datos de Microsoft Access.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUseODBC</strong></p></td>
<td><p>El objeto <strong>Workspace</strong> está conectado a un origen de datos ODBC.</p></td>
</tr>
</tbody>
</table>

