---
title: Connection.OpenRecordset Method (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 584a3e00-7589-90f1-aa6a-5d6116f0b5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194324(v=office.15)
ms:contentKeyID: 48544993
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9fec0e2717c39ea2aeb4a41d7630998c79ce9c52
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872721"
---
# <a name="connectionopenrecordset-method-dao"></a>Connection.OpenRecordset Method (DAO)


**Se aplica a**: Access 2013, Office 2013

Crea un nuevo objeto **[Recordset](recordset-object-dao.md)** y lo anexa a la colección **Recordsets**.

## <a name="syntax"></a>Sintaxis

*expresión* . OpenRecordset (***nombre***, ***tipo***, ***Opciones***, ***LockEdit***)

*expresión* Variable que representa un objeto **Connection** .

### <a name="parameters"></a>Parámetros

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
<th><p>Necesario/Opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Nombre</p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Origen de los registros para el nuevo <strong>Recordset</strong>. El origen puede ser un nombre de tabla o de consulta, o una instrucción SQL que devuelve registros. Para los objetos <strong>Recordset</strong> de tipo tabla en las bases de datos del motor de base de datos de Microsoft Access, el origen solo puede ser un nombre de tabla.  </p></td>
</tr>
<tr class="even">
<td><p>Tipo</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica el tipo de <strong>Recordset</strong> para abrir.</p>

> [!NOTE]
> Si abre un **Recordset** en un área de trabajo de Microsoft Access y no especifica un tipo, **OpenRecordset** crea un **Recordset** de tipo tabla, si es posible. Si especifica una tabla o una consulta vinculada, **OpenRecordset** crea un **Recordset** de tipo conjunto de registros dinámicos.


</td>
</tr>
<tr class="odd">
<td><p>Options</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una combinación de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica las características del nuevo <strong>Recordset</strong>.</p>

> [!NOTE]
> Las constantes **dbConsistent** y **dbInconsistent** son mutuamente excluyentes, y el uso de ambos provoca un error. También se proporciona un argumento lockedits cuando opciones utilizan la constante **dbReadOnly** produce un error.


</td>
</tr>
<tr class="even">
<td><p>LockEdit</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina el bloqueo de <strong>Recordset</strong>.</p>

> [!NOTE]
> Puede usar **dbReadOnly** en el argumento options o en el argumento lockedits, pero no en ambos. Si lo usa para los dos argumentos, ocurre un error en tiempo de ejecución.


</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

Recordset

## <a name="remarks"></a>Comentarios

En general, si el usuario obtiene este error mientras actualiza un registro, el código debe actualizar el contenido de los campos y recuperar los valores recién modificados. Si el error se produce al eliminar un registro, el código puede mostrar los nuevos datos de registros al usuario y un mensaje en el que se indica que los datos han cambiado recientemente. En ese momento, el código puede pedir una confirmación de que aún se desea eliminar el registro.

Debe usar también la constante **dbSeeChanges** si abre un objeto **Recordset** en el área de trabajo de ODBC conectado por el motor de base de datos de Microsoft Access contra una tabla de Microsoft SQL Server 6.0 (o posterior) que tiene una columna IDENTITY o, de lo contrario, puede producirse un error.

Al abrir más de un objeto **Recordset** en un origen de datos ODBC, se puede producir un error si la conexión está ocupada con una llamada **OpenRecordset** anterior. Un modo de solucionar este problema es rellenar completamente el objeto **Recordset** mediante el método **MoveLast** en cuanto se abra el objeto **Recordset**.

Cerrar un objeto **Recordset** con el método **[Close](connection-close-method-dao.md)** lo elimina automáticamente de la colección **Recordsets**.


> [!NOTE]
> Si *origen* hace referencia a una instrucción SQL consta de una cadena que se concatena con un valor no entero, y los parámetros del sistema especifican un carácter decimal que no sean-US como una coma (por ejemplo, strSQL = "PRICE &gt; " &amp; lngPrice y lngPrice = 125,50), se produce un error al intentar abrir el **conjunto de registros**. Esto se debe a que, durante la concatenación, el número se convierte en una cadena con el carácter decimal predeterminado del sistema, y SQL solo acepta los caracteres decimales de Estados Unidos.


