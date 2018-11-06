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
ms.openlocfilehash: 45aa005b7c8337a4c5541ea7217cbdb520bb1725
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997738"
---
# <a name="databasemakereplica-method-dao"></a><span data-ttu-id="4d976-102">Database.MakeReplica (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="4d976-102">Database.MakeReplica method (DAO)</span></span>

<span data-ttu-id="4d976-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d976-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4d976-104">Crea una nueva réplica a partir de otra réplica de base de datos (sólo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="4d976-104">Makes a new replica from another database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="4d976-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d976-105">Syntax</span></span>

<span data-ttu-id="4d976-106">*expresión* . MakeReplica (***nombreruta***, ***Descripción***, ***Opciones***)</span><span class="sxs-lookup"><span data-stu-id="4d976-106">*expression* .MakeReplica(***PathName***, ***Description***, ***Options***)</span></span>

<span data-ttu-id="4d976-107">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="4d976-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="4d976-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d976-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4d976-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="4d976-109">Name</span></span></p></th>
<th><p><span data-ttu-id="4d976-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="4d976-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="4d976-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4d976-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="4d976-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d976-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d976-113"><em>Ruta de acceso</em></span><span class="sxs-lookup"><span data-stu-id="4d976-113"><em>PathName</em></span></span></p></td>
<td><p><span data-ttu-id="4d976-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4d976-114">Required</span></span></p></td>
<td><p><span data-ttu-id="4d976-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="4d976-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="4d976-p101">Ruta de acceso y nombre de archivo de la nueva réplica. Si la réplica es un nombre de archivo existente, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="4d976-p101">The path and file name of the new replica. If replica is an existing file name, then an error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d976-118"><em>Descripción</em></span><span class="sxs-lookup"><span data-stu-id="4d976-118"><em>Description</em></span></span></p></td>
<td><p><span data-ttu-id="4d976-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4d976-119">Required</span></span></p></td>
<td><p><span data-ttu-id="4d976-120"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="4d976-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="4d976-121"><strong>String</strong> que describe la réplica que se va a crear</span><span class="sxs-lookup"><span data-stu-id="4d976-121">A <strong>String</strong> that describes the replica that you are creating</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d976-122"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="4d976-122"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="4d976-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="4d976-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="4d976-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="4d976-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="4d976-125">Constante <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> que especifica las características de la réplica que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="4d976-125">A <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> constant that specifies characteristics of the replica you are creating.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4d976-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d976-126">Remarks</span></span>

<span data-ttu-id="4d976-127">Una réplica parcial recién creada tendrá todas las propiedades **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** establecidas en **False**, lo que indica que no habrá datos en las tablas.</span><span class="sxs-lookup"><span data-stu-id="4d976-127">A newly created partial replica will have all **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** properties set to **False**, meaning that no data will be in the tables.</span></span>

## <a name="example"></a><span data-ttu-id="4d976-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d976-128">Example</span></span>

<span data-ttu-id="4d976-129">Esta función utiliza el método **MakeReplica** para crear una réplica adicional de un diseño principal existente.</span><span class="sxs-lookup"><span data-stu-id="4d976-129">This function uses the **MakeReplica** method to create an additional replica of an existing Design Master.</span></span> <span data-ttu-id="4d976-130">El argumento intOptions puede ser una combinación de las constantes **dbRepMakeReadOnly** y **dbRepMakePartial**, o puede ser 0.</span><span class="sxs-lookup"><span data-stu-id="4d976-130">The intOptions argument can be a combination of the constants **dbRepMakeReadOnly** and **dbRepMakePartial**, or it can be 0.</span></span> <span data-ttu-id="4d976-131">Por ejemplo, para crear una réplica parcial de sólo lectura, debe pasar el valor **dbRepMakeReadOnly** + **dbRepMakePartial** como el valor de intOptions.</span><span class="sxs-lookup"><span data-stu-id="4d976-131">For example, to create a read-only partial replica, you should pass the value **dbRepMakeReadOnly** + **dbRepMakePartial** as the value of intOptions.</span></span>

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

