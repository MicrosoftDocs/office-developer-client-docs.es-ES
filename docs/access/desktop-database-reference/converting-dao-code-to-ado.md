---
title: Convertir código DAO en ADO
TOCTitle: Convert DAO code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 60baeabfce93c2987cb9621c7cc877a7525a954c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876746"
---
# <a name="convert-dao-code-to-ado"></a>Convertir código DAO en ADO

**Se aplica a**: Access 2013, Office 2013

> [!NOTE]
> Versiones de la biblioteca DAO anteriores a 3.6 no se proporcionan ni son compatibles en Access.

## <a name="dao-to-ado-object-map"></a>DAO al mapa de objetos de ADO

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><strong>DAO</strong></p></th>
<th><p><strong>ADO (ADODB)</strong></p></th>
<th><p><strong>Nota</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DBEngine</p></td>
<td><p>Ninguna</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Workspace</p></td>
<td><p>Ninguna</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Base de datos</p></td>
<td><p>Connection</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Recordset</p></td>
<td><p>Recordset</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Dynaset-Type</p></td>
<td><p>Keyset</p></td>
<td><p>Recupera un conjunto de punteros a los registros del objeto Recordset.</p></td>
</tr>
<tr class="even">
<td><p>Snapshot-Type</p></td>
<td><p>Static</p></td>
<td><p>Ambos recuperan registros completos pero puede actualizarse un conjunto de registros estático.</p></td>
</tr>
<tr class="odd">
<td><p>Table-Type</p></td>
<td><p>Keyset con la opción adCmdTableDirect.</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Field</p></td>
<td><p>Field</p></td>
<td><p>Cuando se hace referencia en un conjunto de registros.</p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a>DAO

#### <a name="open-a-recordset"></a>Abrir un objeto Recordset

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a>Modificar un objeto Recordset

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a>ADO

#### <a name="open-a-recordset"></a>Abrir un objeto Recordset

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a>Modificar un objeto Recordset

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> Mover el enfoque desde el registro actual por medio de **MoveNext, MoveLast, MoveFirst, MovePrevious** sin utilizar primero el método **CancelUpdate** implícitamente, ejecuta el método **Update** .

### <a name="about-the-contributors"></a>Acerca de los colaboradores

**Vínculo proporcionado por** la Comunidad [UtterAccess](https://www.utteraccess.com) . UtterAccess es el principal foro de ayuda y wiki sobre Microsoft Access.

- [Elegir entre DAO y ADO](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

