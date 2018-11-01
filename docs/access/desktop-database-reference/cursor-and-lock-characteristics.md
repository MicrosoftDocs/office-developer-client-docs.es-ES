---
title: Características de cursores y bloqueos
TOCTitle: Cursor and Lock Characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 85268b9c4b57d92cd8e7df9cd1da01286709f915
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877572"
---
# <a name="cursor-and-lock-characteristics"></a>Características de cursores y bloqueos


**Se aplica a**: Access 2013, Office 2013

Aunque las características de un cursor dependen de la funcionalidades del proveedor, las ventajas y desventajas siguientes generalmente son de aplicación para los diversos tipos de cursores y bloqueos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de cursor o bloqueo</p></th>
<th><p>Ventajas</p></th>
<th><p>Desventajas</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p></p>
<ul>
<li><p>Pocos requisitos de recursos</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>No se puede efectuar un desplazamiento hacia atrás</p></li>
<li><p>No hay coincidencia de datos</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p></p>
<ul>
<li><p>Desplazable</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>No hay coincidencia de datos</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p></p>
<ul>
<li><p>Hay alguna coincidencia de datos</p></li>
<li><p>Desplazable</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Más requisitos de recursos</p></li>
<li><p>No disponible en escenario de desconexión</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p></p>
<ul>
<li><p>Elevada coincidencia de datos</p></li>
<li><p>Desplazable</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Requisitos de recursos máximos</p></li>
<li><p>No disponible en escenario de desconexión</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockReadOnly</strong></p></td>
<td><p></p>
<ul>
<li><p>Pocos requisitos de recursos</p></li>
<li><p>Altamente escalable</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Datos no actualizables a través de cursor</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLockBatchOptimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Actualizaciones por lotes</p></li>
<li><p>Permite escenarios de desconexión</p></li>
<li><p>Otros usuarios pueden tener acceso a datos</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Varios usuarios pueden cambiar los datos simultáneamente</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockPessimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Otros usuarios no pueden cambiar los datos mientras están bloqueados</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Impide a otros usuarios el acceso a los datos mientras están bloqueados</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLockOptimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Otros usuarios pueden tener acceso a datos</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Varios usuarios pueden cambiar los datos simultáneamente</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

