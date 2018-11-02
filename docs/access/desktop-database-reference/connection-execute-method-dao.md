---
title: Método Connection.Execute (DAO)
TOCTitle: Execute Method
ms:assetid: d6140d4e-fa14-6455-525e-49d8aab3dff7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835040(v=office.15)
ms:contentKeyID: 48547978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a06837ec98d96cc4c6ae75a19dd953ca4dc59dc
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920084"
---
# <a name="connectionexecute-method-dao"></a>Método Connection.Execute (DAO)


**Se aplica a**: Access 2013, Office 2013

Ejecuta una consulta de acción o una instrucción SQL en el objeto especificado.

## <a name="syntax"></a>Sintaxis

*expresión* . Ejecutar (***consulta***, ***Opciones***)

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
<td><p>Query</p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p><strong>String</strong> que es una instrucción SQL o el valor de la propiedad <strong>Name</strong> de un objeto <strong>QueryDef</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Options</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante o combinación de constantes que determinan las características de integridad de los datos, tal como se especifica en la sección de configuración.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Puede usar las siguientes constantes **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** para ver las opciones.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDenyWrite</strong></p></td>
<td><p>Deniega el permiso de escritura a otros usuarios (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInconsistent</strong></p></td>
<td><p>(Valor predeterminado) Ejecuta actualizaciones no coherentes (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbConsistent</strong></p></td>
<td><p>Ejecuta actualizaciones coherentes (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSQLPassThrough</strong></p></td>
<td><p>Ejecuta una consulta de paso a través de SQL. Establecer esta opción pasa la instrucción SQL a una base de datos ODBC para procesamiento (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFailOnError</strong></p></td>
<td><p>Deshace las actualizaciones si se produce un error (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSeeChanges</strong></p></td>
<td><p>Genera un error en tiempo de ejecución si otro usuario cambia los datos que está usted editando (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Ejecuta la consulta de forma asincrónica (sólo conexiones ODBCDirect y objetos QueryDef).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbExecDirect</strong></p></td>
<td><p>Ejecuta la instrucción sin llamar primero a la función API de ODBC SQLPrepare (sólo conexiones ODBCDirect y objetos QueryDef).</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.

> [!NOTE]
> [!NOTA] Las constantes **dbConsistent** y **dbInconsistent** son mutuamente excluyentes. Puede usar una o la otra, pero no ambas, en una instancia específica de **OpenRecordset**. Si se usan **dbConsistent** y **dbInconsistent**, se produce un error.

El método **Execute** solo es válido para consultas de acción. Si utiliza **Execute** con otro tipo de consulta, se produce un error. Como una consulta de acción no devuelve registros, **Execute** no devuelve un objeto **Recordset**. (La ejecución de una consulta de paso SQL en un área de trabajo de ODBCDirect no devuelve un error si no se devuelve un objeto **Recordset**.)

Utilice la propiedad **RecordsAffected** del objeto **Connection**, **Database** o **QueryDef** para determinar el número de registros afectados por el método **Execute** más reciente. Por ejemplo, **RecordsAffected** contiene el número de registros eliminados, actualizados o insertados al ejecutar una consulta de acción. Cuando se utiliza el método **Execute** para ejecutar una consulta, la propiedad **RecordsAffected** del objeto **QueryDef** se establece en el número de registros afectados.

En un área de trabajo de Microsoft Access, si especifica una instrucción SQL sintácticamente correcta y dispone de los permisos correspondientes, el método **Execute** no producirá un error, aunque no pueda modificarse ni eliminarse una fila. Por tanto, utilice siempre la opción **dbFailOnError** cuando use el método **Execute** para ejecutar una actualización o eliminar una consulta. Esta opción genera un error en tiempo de ejecución y deshace todos los cambios que se han realizado correctamente si alguno de los registros afectados está bloqueado y no se puede actualizar o eliminar.

En versiones anteriores del motor de base de datos de Microsoft Jet, las instrucciones SQL se insertaban automáticamente en transacciones implícitas. Si parte de una instrucción ejecutada con **dbFailOnError** producía un error, se revertía toda la instrucción. Para mejorar el rendimiento, desde la versión 3.5 estas instrucciones implícitas ya no existen. Si actualiza código DAO antiguo, no olvide que debe usar transacciones explícitas con las instrucciones **Execute**.

Para mejorar el rendimiento en un área de trabajo de Microsoft Access, especialmente en un entorno multiusuario, anide el método **Execute** dentro de una transacción. Utilice el método **BeginTrans** en el objeto **Workspace** actual y, a continuación, utilice el método **Execute** y complete la transacción empleando el método **CommitTrans** en el objeto **Workspace**. De esta forma, se reducirán los cambios en disco y se liberarán todos los bloqueos aplicados mientras se ejecuta la consulta.

