---
title: Sección de los registros del archivo de personalización
TOCTitle: Customization File Logs section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c9a8b9c2255825b135fbc181900a73b3686c64c7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946156"
---
# <a name="customization-file-logs-section"></a>Sección de los registros del archivo de personalización

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

