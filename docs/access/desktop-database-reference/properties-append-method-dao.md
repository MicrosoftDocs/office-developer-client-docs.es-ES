---
title: Método Properties.Append (DAO)
TOCTitle: Append Method
ms:assetid: 47f1e24f-975c-3fdc-5c3c-8c91f2920c81
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193232(v=office.15)
ms:contentKeyID: 48544609
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 528809495ebefd15a8895b15a9d51f84e6892980
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301312"
---
# <a name="propertiesappend-method-dao"></a>Método Properties.Append (DAO)

**Se aplica a:** Access 2013, Office 2013

Agrega un nuevo objeto **Property** a la colección **Properties**.

## <a name="syntax"></a>Sintaxis

*expression* .Append(***Object***)

*expresión* Variable que representa un objeto **Properties** .

## <a name="parameters"></a>Parámetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Objeto</em></p></td>
<td><p>Necesario</p></td>
<td><p><strong>Objeto</strong></p></td>
<td><p>Variable de objeto que representa el campo que se va a anexar a la colección.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

El objeto anexado se convierte en un objeto persistente, almacenado en un disco, hasta que lo elimine mediante el método **Delete**.

La agregación de un nuevo objeto se produce de inmediato pero debe utilizar el método **Refresh** en cualquier otra colección que pueda verse afectada por los cambios en la estructura de base de datos.

Si el objeto que está anexando está incompleto (como cuando no ha anexado ningún objeto **Field** a una colección **Fields** de un objeto **Index** antes de anexarlo a una colección **Indexes**) o si las propiedades establecidas en uno o varios objetos subordinados son incorrectas, el uso del método **Append** provoca un error. Por ejemplo, si no ha especificado un campo e intenta anexar el objeto **Field** a la colección **Fields** en un objeto **TableDef**, el uso del método **Append** desencadena un error en tiempo de ejecución.

