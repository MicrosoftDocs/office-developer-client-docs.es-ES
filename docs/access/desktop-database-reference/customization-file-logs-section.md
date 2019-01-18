---
title: Sección de registros de archivo de personalización
TOCTitle: Customization File Logs section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a9af5d09a7a7a7a7ec97d757d502efbf2402900
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715637"
---
# <a name="customization-file-logs-section"></a>Sección de registros de archivo de personalización

**Se aplica a**: Access 2013, Office 2013

La sección **Logs** contiene una entrada de archivo de registro, que especifica el nombre de un archivo que registra los errores durante el funcionamiento de **DataFactory**.

## <a name="syntax"></a>Sintaxis

Una entrada de archivo de registro tiene el siguiente formato:

`err=FileName`

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Elemento</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>err</strong></p></td>
<td><p>Cadena literal que indica que se trata de una entrada de archivo de registro.</p></td>
</tr>
<tr class="even">
<td><p><em>FileName</em></p></td>
<td><p>Nombre y ruta de acceso completos. El nombre de archivo suele ser <strong> c:\msdfmap.log</strong>.</p></td>
</tr>
</tbody>
</table>


El archivo de registro contiene el nombre de usuario, HRESULT, la fecha y la hora de cada error.

