---
title: Espacios de nombres (referencia de base de datos de escritorio de Access)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 905edba502fcc2994be6f6b8e50a7200b66a82b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288628"
---
# <a name="namespaces"></a>Espacios de nombres

**Se aplica a:** Access 2013, Office 2013

El formato XML persistente en ADO utiliza los cuatro espacios de nombres siguientes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Prefix</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>s</p></td>
<td><p>Hace referencia al espacio &quot; de nombres XML-Data &quot; que contiene los elementos y atributos que definen el esquema del objeto Recordset <strong>actual.</strong></p></td>
</tr>
<tr class="even">
<td><p>dt</p></td>
<td><p>Hace referencia a la especificación de definiciones de tipos de datos.</p></td>
</tr>
<tr class="odd">
<td><p>rs</p></td>
<td><p>Hace referencia al espacio de nombres que contiene elementos y atributos específicos de propiedades y atributos del <strong>conjunto de registros</strong> de ADO.</p></td>
</tr>
<tr class="even">
<td><p>z</p></td>
<td><p>Hace referencia al esquema del conjunto de filas activo.</p></td>
</tr>
</tbody>
</table>


Un cliente no debe agregar sus propias etiquetas a estos espacios de nombres, según se define en las especificaciones. Por ejemplo, un cliente no debe definir un espacio de nombres como "urn:schemas-microsoft-com:rowset" y luego escribir algo como "rs:MiEtiqueta". Para obtener más información acerca de espacios de nombres, vea [Espacios de nombres XML](https://www.w3.org/tr/xml-names/).

> [!NOTE]
> [!NOTA] El identificador para la etiqueta del esquema debe ser "RowsetSchema" y el espacio de nombres utilizado para hacer referencia al esquema del conjunto de filas activo debe apuntar a "#RowsetSchema".

Tenga en cuenta que el prefijo del espacio de nombres, que parte a la derecha de la coma y a la izquierda del signo igual, es arbitrario.

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

El usuario puede definirlo de modo que sea cualquier nombre, siempre que este nombre se utilice incoherentemente en todo el documento XML. ADO siempre escribe "s" "rs" "dt" y "z", pero estos nombres de prefijos no se codifican de forma rígida en el componente de carga.



