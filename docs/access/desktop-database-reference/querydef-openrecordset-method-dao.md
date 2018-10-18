---
title: QueryDef.OpenRecordset Method (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 368c59f0ea207862c5b7ac5ea7f664295adb5188
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606839"
---
# <a name="querydefopenrecordset-method-dao"></a>QueryDef.OpenRecordset Method (DAO)


**Se aplica a**: Access 2013 | Office 2013

Crea un nuevo objeto **[Recordset](recordset-object-dao.md)** y lo anexa a la colección **Recordsets**.

## <a name="syntax"></a>Sintaxis

*expresión* . OpenRecordset (***tipo***, ***Opciones***, ***LockEdit***)

*expresión* Variable que representa un objeto **QueryDef** .

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
<td><p>Tipo</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica el tipo de <strong>Recordset</strong> para abrir.</p>

> [!NOTE]
> <P>Si abre un <STRONG>Recordset</STRONG> en un área de trabajo de Microsoft Access y no especifica un tipo, <STRONG>OpenRecordset</STRONG> crea un <STRONG>Recordset</STRONG> de tipo tabla, si es posible. Si especifica una tabla o una consulta vinculada, <STRONG>OpenRecordset</STRONG> crea un <STRONG>Recordset</STRONG> de tipo conjunto de registros dinámicos.</P>


</td>
</tr>
<tr class="even">
<td><p>Options</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una combinación de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica las características del nuevo <strong>Recordset</strong>.</p>

> [!NOTE]
> <P>Las constantes <STRONG>dbConsistent</STRONG> y <STRONG>dbInconsistent</STRONG> son mutuamente exclusivas, y usar las dos producirá un error. Proporcionar un argumento lockedits cuando las opciones usan la constante <STRONG>dbReadOnly</STRONG> también produce un error.</P>


</td>
</tr>
<tr class="odd">
<td><p>LockEdit</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina el bloqueo de <strong>Recordset</strong>.</p>

> [!NOTE]
> <P>Puede usar <STRONG>dbReadOnly</STRONG> en el argumento options o en el argumento lockedits, pero no en ambos. Si lo usa para los dos argumentos, ocurre un error en tiempo de ejecución.</P>


</td>
</tr>
</tbody>
</table>


<<<<<<< HEAD
### <a name="return-value"></a>Valor devuelto
=======
### <a name="return-value"></a>Valor devuelto
>>>>>>> master

Recordset

## <a name="remarks"></a>Observaciones

Debe usar también la constante **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** si abre un objeto **Recordset** en el área de trabajo de ODBC conectado por el motor de base de datos de Microsoft Access contra una tabla de Microsoft SQL Server 6.0 (o posterior) que tiene una columna IDENTITY o, de lo contrario, puede producirse un error.

Al abrir más de un objeto **Recordset** en un origen de datos ODBC, se puede producir un error si la conexión está ocupada con una llamada **OpenRecordset** anterior. Un modo de solucionar este problema es rellenar completamente el objeto **Recordset** mediante el método **[MoveLast](recordset-movelast-method-dao.md)** en cuanto se abra el objeto **Recordset**.

Cerrar un objeto **Recordset** con el método **Close** lo elimina automáticamente de la colección **Recordsets**.


> [!NOTE]
> <P>Si <EM>origen</EM> hace referencia a una instrucción SQL consta de una cadena que se concatena con un valor no entero, y los parámetros del sistema especifican un carácter decimal que no sean-US como una coma (por ejemplo, strSQL = "PRICE &gt; " &amp; lngPrice y lngPrice = 125,50), se produce un error al intentar abrir el <STRONG>conjunto de registros</STRONG>. Esto se debe a que, durante la concatenación, el número se convierte en una cadena con el carácter decimal predeterminado del sistema, y SQL solo acepta los caracteres decimales de Estados Unidos.</P>


