---
title: Database.MakeReplica (método) (DAO)
TOCTitle: MakeReplica Method
ms:assetid: b6bf4982-0804-12ce-849f-d2b4ac2e48a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822413(v=office.15)
ms:contentKeyID: 48547286
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053371
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a47709d1be3eab66f849e076c5756d5081d28fc8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930234"
---
# <a name="databasemakereplica-method-dao"></a>Database.MakeReplica (método) (DAO)

**Se aplica a**: Access 2013, Office 2013

Crea una nueva réplica a partir de otra réplica de base de datos (sólo en áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . MakeReplica (***nombreruta***, ***Descripción***, ***Opciones***)

*expresión* Variable que representa un objeto de **base de datos** .

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
<td><p>Ruta de acceso</p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Ruta de acceso y nombre de archivo de la nueva réplica. Si la réplica es un nombre de archivo existente, se produce un error.</p></td>
</tr>
<tr class="even">
<td><p>Descripción</p></td>
<td><p>Necesario</p></td>
<td><p><strong>String</strong></p></td>
<td><p><strong>String</strong> que describe la réplica que se va a crear</p></td>
</tr>
<tr class="odd">
<td><p>Options</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> que especifica las características de la réplica que se va a crear.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Una réplica parcial recién creada tendrá todas las propiedades **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** establecidas en **False**, lo que indica que no habrá datos en las tablas.

## <a name="example"></a>Ejemplo

Esta función utiliza el método **MakeReplica** para crear una réplica adicional de un diseño principal existente. El argumento intOptions puede ser una combinación de las constantes **dbRepMakeReadOnly** y **dbRepMakePartial**, o puede ser 0. Por ejemplo, para crear una réplica parcial de sólo lectura, debe pasar el valor **dbRepMakeReadOnly** + **dbRepMakePartial** como el valor de intOptions.

```vb 
Function MakeAdditionalReplica(strReplicableDB As _ 
 String, strNewReplica As String, intOptions As _ 
 Integer) As Integer 
 
 Dim dbsTemp As Database 
 On Error GoTo ErrorHandler 
 
 Set dbsTemp = OpenDatabase(strReplicableDB) 
 
 ' If no options are passed to 
 ' MakeAdditionalReplica, omit the 
 ' options argument, which defaults to 
 ' a full, read/write replica. Otherwise, 
 ' use the value of intOptions. 
 
 If intOptions = 0 Then 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB 
 Else 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB, _ 
 intOptions 
 End If 
 
 dbsTemp.Close 
 
ErrorHandler: 
 Select Case Err 
 Case 0: 
 MakeAdditionalReplica = 0 
 Exit Function 
 Case Else: 
 MsgBox "Error " & Err & " : " & Error 
 MakeAdditionalReplica = Err 
 Exit Function 
 End Select 
 
End Function 
 
```

