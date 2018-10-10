---
title: Espacios de nombres (referencia de escritorio de la base de datos de Access)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dc7c0cf302c0b8a297310dfa439ac87724331569
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485484"
---
# <a name="namespaces"></a>Espacios de nombres


**Se aplica a**: Access 2013 | Office 2013

## <a name="namespaces"></a>Espacios de nombres

El formato XML persistente en ADO utiliza los cuatro espacios de nombres siguientes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Prefijo</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>s</p></td>
<td><p>Hace referencia a la &quot;datos XML&quot; espacio de nombres que contiene los elementos y atributos que definen el esquema del <strong>conjunto de registros</strong>actual.</p></td>
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
> <P>[!NOTA] El identificador para la etiqueta del esquema debe ser "RowsetSchema" y el espacio de nombres utilizado para hacer referencia al esquema del conjunto de filas activo debe apuntar a "#RowsetSchema".</P>



Tenga en cuenta que el prefijo del espacio de nombres, que parte a la derecha de la coma y a la izquierda del signo igual, es arbitrario.

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

El usuario puede definirlo de modo que sea cualquier nombre, siempre que este nombre se utilice incoherentemente en todo el documento XML. ADO siempre escribe "s" "rs" "dt" y "z", pero estos nombres de prefijos no se codifican de forma rígida en el componente de carga.

## <a name="namespaces"></a>Espacios de nombres

El formato XML persistente en ADO utiliza los cuatro espacios de nombres siguientes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Prefijo</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>s</p></td>
<td><p>Hace referencia a la &quot;datos XML&quot; espacio de nombres que contiene los elementos y atributos que definen el esquema del <strong>conjunto de registros</strong>actual.</p></td>
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
> <P>[!NOTA] El identificador para la etiqueta del esquema debe ser "RowsetSchema" y el espacio de nombres utilizado para hacer referencia al esquema del conjunto de filas activo debe apuntar a "#RowsetSchema".</P>



Tenga en cuenta que el prefijo del espacio de nombres, que parte a la derecha de la coma y a la izquierda del signo igual, es arbitrario.

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

El usuario puede definirlo de modo que sea cualquier nombre, siempre que este nombre se utilice incoherentemente en todo el documento XML. ADO siempre escribe "s" "rs" "dt" y "z", pero estos nombres de prefijos no se codifican de forma rígida en el componente de carga.

