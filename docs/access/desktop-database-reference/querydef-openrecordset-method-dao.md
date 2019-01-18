---
title: QueryDef.OpenRecordset (método) (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a046359f39611e38b9e517495f54041f876addfc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710247"
---
# <a name="querydefopenrecordset-method-dao"></a>QueryDef.OpenRecordset (método) (DAO)

**Se aplica a**: Access 2013, Office 2013

Crea un nuevo objeto **[Recordset](recordset-object-dao.md)** y lo anexa a la colección **Recordsets**.

## <a name="syntax"></a>Sintaxis

*expresión* . OpenRecordset (***tipo***, ***Opciones***, ***LockEdit***)

*expresión* Variable que representa un objeto **QueryDef** .

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
<td><p><em>Type</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica el tipo de <strong>Recordset</strong> para abrir.</p><p><strong>Nota</strong>: si se abre un <STRONG>objeto Recordset</STRONG> en un área de trabajo de Microsoft Access y no especifica ningún tipo, <STRONG>OpenRecordset</STRONG> crea un <STRONG>objeto Recordset</STRONG>de tipo tabla, si es posible. Si se especifica una tabla vinculada o consulta, <STRONG>OpenRecordset</STRONG> crea un <STRONG>objeto Recordset</STRONG>de tipo dynaset.</p>
</td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una combinación de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica las características del nuevo <strong>Recordset</strong>.</p></p><p><strong>Nota</strong>: las constantes <STRONG>dbConsistent</STRONG> y <STRONG>dbInconsistent</STRONG> son mutuamente excluyentes, y el uso de ambos provoca un error. También se proporciona un argumento lockedits cuando options utiliza la constante <STRONG>dbReadOnly</STRONG> , producirá un error.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>LockEdit</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina el bloqueo de <strong>Recordset</strong>.</p></p><p><strong>Nota</strong>: puede utilizar <STRONG>dbReadOnly</STRONG> en el argumento options o lockedits, pero no ambos. Si usa para ambos argumentos, se produce un error en tiempo de ejecución.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor devuelto

Recordset

## <a name="remarks"></a>Observaciones

Debe usar también la constante **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** si abre un objeto **Recordset** en el área de trabajo de ODBC conectado por el motor de base de datos de Microsoft Access contra una tabla de Microsoft SQL Server 6.0 (o posterior) que tiene una columna IDENTITY o, de lo contrario, puede producirse un error.

Al abrir más de un objeto **Recordset** en un origen de datos ODBC, se puede producir un error si la conexión está ocupada con una llamada **OpenRecordset** anterior. Un modo de solucionar este problema es rellenar completamente el objeto **Recordset** mediante el método **[MoveLast](recordset-movelast-method-dao.md)** en cuanto se abra el objeto **Recordset**.

Cerrar un objeto **Recordset** con el método **Close** lo elimina automáticamente de la colección **Recordsets**.

> [!NOTE]
> Si *origen* hace referencia a una instrucción SQL consta de una cadena que se concatena con un valor no entero, y los parámetros del sistema especifican un carácter decimal que no sean-US como una coma (por ejemplo, strSQL = "PRICE &gt; " &amp; lngPrice y lngPrice = 125,50), se produce un error al intentar abrir el **conjunto de registros**. Esto se debe a que, durante la concatenación, el número se convierte en una cadena con el carácter decimal predeterminado del sistema, y SQL solo acepta los caracteres decimales de Estados Unidos.


