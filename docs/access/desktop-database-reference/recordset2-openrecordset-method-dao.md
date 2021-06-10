---
title: Método Recordset2.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: da6ce86e-957e-21f8-07ac-8acd57326a12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835325(v=office.15)
ms:contentKeyID: 48548082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 08120f4ebb6b2d9989051171a0c71b6d9fcf6e5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307255"
---
# <a name="recordset2openrecordset-method-dao"></a>Método Recordset2.OpenRecordset (DAO)

**Se aplica a:** Access 2013, Office 2013

Crea un nuevo objeto **[Recordset](recordset-object-dao.md)** y lo anexa a la colección **Recordsets**.

## <a name="syntax"></a>Sintaxis

*expression* .OpenRecordset(***Type***, ***Options***)

*expresión* Variable que representa un **objeto Recordset2.**

## <a name="parameters"></a>Parameters

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
<td><p><em>Name</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Origen de los registros para el nuevo <strong>Recordset</strong>. El origen puede ser un nombre de tabla o de consulta, o una instrucción SQL que devuelve registros. Para los objetos <strong>Recordset</strong> de tipo tabla en las bases de datos del motor de base de datos de Microsoft Access, el origen solo puede ser un nombre de tabla.</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica el tipo de <strong>Recordset</strong> para abrir.</p><p><strong>NOTA</strong>: si abre un <STRONG>Recordset</STRONG> en un área de trabajo de Microsoft Access y no especifica un tipo, <STRONG>OpenRecordset</STRONG> crea un <STRONG>Recordset</STRONG> de tipo tabla, si es posible. If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>Opciones</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una combinación de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifican características del nuevo <strong>Recordset</strong>.</p><p><strong>NOTA</strong>: las constantes <STRONG>dbConsistent</STRONG> y <STRONG>dbInconsistent</STRONG> son mutuamente exclusivas, y usar las dos producirá un error. Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</p>
</td>
</tr>
<tr class="even">
<td><p><em>LockEdit</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina el bloqueo del <strong>Recordset</strong>.</p><p><strong>NOTA</strong>: Puede usar <STRONG>dbReadOnly</STRONG> en el argumento options o en el argumento lockedits, pero no en ambos. Si lo usa para ambos argumentos, se produce un error en tiempo de ejecución.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor devuelto

Recordset

## <a name="remarks"></a>Observaciones

En general, si el usuario obtiene este error mientras actualiza un registro, el código debe actualizar el contenido de los campos y recuperar los valores recién modificados. Si el error se produce al eliminar un registro, el código puede mostrar los nuevos datos de registros al usuario y un mensaje en el que se indica que los datos han cambiado recientemente. En ese momento, el código puede pedir una confirmación de que aún se desea eliminar el registro.

Debe usar también la constante **dbSeeChanges** si abre un objeto **Recordset** en el área de trabajo de ODBC conectado por el motor de base de datos de Microsoft Access contra una tabla de Microsoft SQL Server 6.0 (o posterior) que tiene una columna IDENTITY o, de lo contrario, puede producirse un error.

Al abrir más de un objeto **Recordset** en un origen de datos ODBC, se puede producir un error si la conexión está ocupada con una llamada **OpenRecordset** anterior. Un modo de solucionar este problema es rellenar completamente el objeto **Recordset** mediante el método **MoveLast** en cuanto se abra el objeto **Recordset**.

Cerrar un objeto **Recordset** con el método **[Close](connection-close-method-dao.md)** lo elimina automáticamente de la colección **Recordsets**.

> [!NOTE]
> Si *origen* hace referencia a una instrucción SQL compuesta por una cadena concatenada con un valor de tipo no entero y los parámetros del sistema especifican un carácter decimal que no es de EE.UU., como una coma (por ejemplo, strSQL = "PRICE &gt; " &amp; lngPrice e lngPrice = 125,50), se produce un error cuando intenta abrir **Recordset**. Esto se debe a que durante la concatenación, el número se convierte en una cadena que usa el carácter decimal predeterminado de su sistema y SQL solo acepta caracteres decimales de EE.UU.


